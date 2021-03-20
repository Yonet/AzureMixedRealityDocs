# How to add Virtual Reality capabilities to your app?

We need to add an environment and create an XR Experience. This will automaticly add a button to our scene to go into VR mode.

```typescript
    const env = scene.createDefaultEnvironment();

    const xr = await scene.createDefaultXRExperienceAsync({
        floorMeshes: [env.ground]
    });
```

{% embed url="https://playground.babylonjs.com/\#F41V6N" %}

We can also add the WebXR directly to a loaded model without an environment.



```text
// Async call
BABYLON.SceneLoader.Append("https://www.babylonjs.com/Scenes/Mansion/",
    "Mansion.babylon", scene, async function  () {
        var xr = await scene.createDefaultXRExperienceAsync({floorMeshes: [scene.getMeshByName("Allée")]});
    });
    
```

{% embed url="https://playground.babylonjs.com/\#JA1ND3\#161" %}





