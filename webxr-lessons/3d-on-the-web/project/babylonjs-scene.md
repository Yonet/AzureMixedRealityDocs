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
**Scene** object gets **engine** as the input argument. You don't have to worry about the engine when you are working on the playground but when you are working on your local code sample, we will create the engine as well.
{% endhint %}

 ****_**Arc Rotate Camera**_  ****acts like a satellite in orbit around a target and always points towards the target position. In our case, it is pointing towards the box. Where ever you move your camera, it will still point to towards the box. 

Arc Rotate Camera parameters are: **name** you want to give to your camera, **alpha**\(radians\) the longitudinal rotation, **beta** _beta_ \(radians\) the latitudinal rotation, **radius\(**the distance from the target position\), **target position**\(center where the box will be created as a default\), **scene**\(optional argument\). In this code example scene is not given as an argument and defaults to the scene object on the playground. 

![Arc Rotate Camera parameters: alpha, beta, radius and target position.](../../../.gitbook/assets/camalphabeta.jpg)

{% hint style="info" %}
 Setting _beta_ to 0 or PI can, for technical reasons, cause problems.
{% endhint %}

