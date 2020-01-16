# How to save the new CloudSpatialAnchor as a WorldAnchor on the local platform?

Attach a local **Azure Spatial Anchor** to the **sphere** that we're placing in the real world.

```csharp
/// <summary>
/// Creates a sphere at the hit point, and then saves a CloudSpatialAnchor there.
/// </summary>
/// <param name="hitPoint">The hit point.</param>
protected virtual void CreateAndSaveSphere(Vector3 hitPoint)
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
}
```

