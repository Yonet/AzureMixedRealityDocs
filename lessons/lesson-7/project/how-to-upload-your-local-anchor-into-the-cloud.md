# How to upload your local Anchor into the cloud?

Add **task.run** function on **line 26** to your **CreateAndSaveAnchor** function. We will change the color of the sphere to indicate that it is saved or failed to save.

```csharp
/// <summary>
    /// Creates a sphere at the hit point, and then saves a CloudSpatialAnchor there.
    /// </summary>
    /// <param name="hitPoint">The hit point.</param>
    protected virtual void CreateAndSaveAnchor(Vector3 hitPoint)
    {
        // Create a white sphere.
        sphere = GameObject.Instantiate(spherePrefab, hitPoint, Quaternion.identity) as GameObject;
        sphere.AddComponent<WorldAnchor>();
        sphereMaterial = sphere.GetComponent<MeshRenderer>().material;
        sphereMaterial.color = Color.white;
        Debug.Log("ASA Info: Created a local anchor.");

        // Create the CloudSpatialAnchor.
        currentCloudAnchor = new CloudSpatialAnchor();

        // Set the LocalAnchor property of the CloudSpatialAnchor to the WorldAnchor component of our white sphere.
        WorldAnchor worldAnchor = sphere.GetComponent<WorldAnchor>();
        if (worldAnchor == null)
        {
            throw new Exception("ASA Error: Couldn't get the local anchor pointer.");
        }

        // Save the CloudSpatialAnchor to the cloud.
        currentCloudAnchor.LocalAnchor = worldAnchor.GetNativeSpatialAnchorPtr();
        Task.Run(async () =>
        {
            // Wait for enough data about the environment.
            while (recommendedForCreate < 1.0F)
            {
                await Task.Delay(330);
            }

            bool success = false;
            try
            {
                QueueOnUpdate(() =>
                {
                    // We are about to save the CloudSpatialAnchor to the Azure Spatial Anchors, turn it yellow.
                    sphereMaterial.color = Color.yellow;
                });

                await cloudSpatialAnchorSession.CreateAnchorAsync(currentCloudAnchor);
                success = currentCloudAnchor != null;

                if (success)
                {
                    // Allow the user to tap again to clear state and look for the anchor.
                    tapExecuted = false;

                    // Record the identifier to locate.
                    cloudSpatialAnchorId = currentCloudAnchor.Identifier;

                    QueueOnUpdate(() =>
                    {
                        // Turn the sphere blue.
                        sphereMaterial.color = Color.blue;
                    });

                    Debug.Log("ASA Info: Saved anchor to Azure Spatial Anchors! Identifier: " + cloudSpatialAnchorId);
                }
                else
                {
                    sphereMaterial.color = Color.red;
                    Debug.LogError("ASA Error: Failed to save, but no exception was thrown.");
                }
            }
            catch (Exception ex)
            {
                QueueOnUpdate(() =>
                {
                    sphereMaterial.color = Color.red;
                });
                Debug.LogError("ASA Error: " + ex.Message);
            }
        });
    }
}
```

