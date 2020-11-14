---
description: Basic Scene with a cube
---

# BabylonJS Scene

To create a basic scene, we initialize a **scene**, create **camera,** **light** and a **mesh** and return the scene object.

#### BabylonJS code

```text
const createScene =  () => {
    const scene = new BABYLON.Scene(engine);

    const camera = new BABYLON.ArcRotateCamera("camera", -Math.PI / 2, Math.PI / 2.5, 3, new BABYLON.Vector3(0, 0, 0));

    const light = new BABYLON.HemisphericLight("light", new BABYLON.Vector3(0, 1, 0));

    const box = BABYLON.MeshBuilder.CreateBox("box", {});

    return scene;
}
```

Live code on babylon playground: [https://playground.babylonjs.com/\#KBS9I5\#158](https://playground.babylonjs.com/#KBS9I5#158)

{% hint style="info" %}
Scene object gets **engine** as the input. You don't have to worry about the engine when you are working on the playground but when you are working on your local code sample, we will create the engine as well.
{% endhint %}

