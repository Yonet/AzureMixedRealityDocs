# How to add ASA script to your scene?

* Create a new script called AzureSpatialAnchorsScript.
* Add imports:

```csharp
using System;
using System.Collections.Generic;
using System.Threading.Tasks;
using UnityEngine;
using UnityEngine.XR.WSA;
using UnityEngine.XR.WSA.Input;
```

* Add the following members variables into your AzureSpatialAnchorsScript class:

```csharp
public class AzureSpatialAnchorsScript : MonoBehaviour
{   
    /// <summary>
    /// The sphere prefab.
    /// </summary>
    public GameObject spherePrefab;

    /// <summary>
    /// Set this string to the Spatial Anchors account id provided in the Spatial Anchors resource.
    /// </summary>
    protected string SpatialAnchorsAccountId = "Set me";

    /// <summary>
    /// Set this string to the Spatial Anchors account key provided in the Spatial Anchors resource.
    /// </summary>
    protected string SpatialAnchorsAccountKey = "Set me";

    /// <summary>
    /// Use the recognizer to detect air taps.
    /// </summary>
    private GestureRecognizer recognizer;

    /// <summary>
    /// True if we are 1) creating + saving an anchor or 2) looking for an anchor.
    /// </summary>
    protected bool tapExecuted = false;

    /// <summary>
    /// The ID of the CloudSpatialAnchor that was saved. Use it to find the CloudSpatialAnchor
    /// </summary>
    protected string cloudSpatialAnchorId = "";

    /// <summary>
    /// The sphere rendered to show the position of the CloudSpatialAnchor.
    /// </summary>
    protected GameObject sphere;
    protected Material sphereMaterial;

    /// <summary>
    /// Indicate if we are ready to save an anchor. We can save an anchor when value is greater than 1.
    /// </summary>
    protected float recommendedForCreate = 0;
```

