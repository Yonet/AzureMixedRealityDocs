# How to initialize a CloudSpatialAnchorSession?

* Import AzureSpacialAnchors asset into your script.

```csharp
using Microsoft.Azure.SpatialAnchors;
```

*  Add the CloudSpatialAnchorSession and CloudSpatialAnchor member variables into your `AzureSpatialAnchorsScript` class:

```csharp
/// <summary>
/// Use the recognizer to detect air taps.
/// </summary>
private GestureRecognizer recognizer;

protected CloudSpatialAnchorSession cloudSpatialAnchorSession;

/// <summary>
/// The CloudSpatialAnchor that we either 1) placed and are saving or 2) just located.
/// </summary>
protected CloudSpatialAnchor currentCloudAnchor;

/// <summary>
/// True if we are 1) creating + saving an anchor or 2) looking for an anchor.
/// </summary>
protected bool tapExecuted = false;
```

* Initialize Session:

```csharp
/// <summary>
/// Initializes a new CloudSpatialAnchorSession.
/// </summary>
void InitializeSession()
{
    Debug.Log("ASA Info: Initializing a CloudSpatialAnchorSession.");

    if (string.IsNullOrEmpty(SpatialAnchorsAccountId))
    {
        Debug.LogError("No account id set.");
        return;
    }

    if (string.IsNullOrEmpty(SpatialAnchorsAccountKey))
    {
        Debug.LogError("No account key set.");
        return;
    }

    cloudSpatialAnchorSession = new CloudSpatialAnchorSession();

    cloudSpatialAnchorSession.Configuration.AccountId = SpatialAnchorsAccountId.Trim();
    cloudSpatialAnchorSession.Configuration.AccountKey = SpatialAnchorsAccountKey.Trim();

    cloudSpatialAnchorSession.LogLevel = SessionLogLevel.All;

    cloudSpatialAnchorSession.Error += CloudSpatialAnchorSession_Error;
    cloudSpatialAnchorSession.OnLogDebug += CloudSpatialAnchorSession_OnLogDebug;
    cloudSpatialAnchorSession.SessionUpdated += CloudSpatialAnchorSession_SessionUpdated;

    cloudSpatialAnchorSession.Start();

    Debug.Log("ASA Info: Session was initialized.");
}
```

* Add methods to handle delegate calls.

```csharp
private void CloudSpatialAnchorSession_Error(object sender, SessionErrorEventArgs args)
{
    Debug.LogError("ASA Error: " + args.ErrorMessage );
}

private void CloudSpatialAnchorSession_OnLogDebug(object sender, OnLogDebugEventArgs args)
{
    Debug.Log("ASA Log: " + args.Message);
    System.Diagnostics.Debug.WriteLine("ASA Log: " + args.Message);
}

private void CloudSpatialAnchorSession_SessionUpdated(object sender, SessionUpdatedEventArgs args)
{
    Debug.Log("ASA Log: recommendedForCreate: " + args.Status.RecommendedForCreateProgress);
    recommendedForCreate = args.Status.RecommendedForCreateProgress;
}
```

Call the InitializeSession method inside the Start\(\) function:

```csharp
// Start is called before the first frame update
void Start()
{
    recognizer = new GestureRecognizer();

    recognizer.StartCapturingGestures();

    recognizer.SetRecognizableGestures(GestureSettings.Tap);

    recognizer.Tapped += HandleTap;

    InitializeSession();
}
```

