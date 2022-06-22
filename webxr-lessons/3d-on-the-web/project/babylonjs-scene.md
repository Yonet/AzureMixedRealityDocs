---
description: Basic Scene with a cube
---

# BabylonJS Scene

### Overview

We will create our BabylonJS scene on Babylon Playground. Find out more about the editor on [What is playground?](../../babylon.js/concepts/what-is-playground.md) chapter.

We will implement the 3D concepts we discussed in [How to create a basic 3D scene?](how-to-create-a-basic-3d-scene.md) chapter.&#x20;

### BabylonJS Code

To create a basic BabylonJS scene, we initialize a **scene**, create **camera,** **light** and a **mesh** and return the scene object.

```typescript
const createScene =  () => {
    const scene = new BABYLON.Scene(engine);

    const camera = new BABYLON.ArcRotateCamera("camera", -Math.PI / 2, Math.PI / 2.5, 3, new BABYLON.Vector3(0, 0, 0));

    const light = new BABYLON.HemisphericLight("light", new BABYLON.Vector3(0, 1, 0));

    const box = BABYLON.MeshBuilder.CreateBox("box", {});

    return scene;
}
```

{% embed url="https://playground.babylonjs.com/#KBS9I5#158" %}
BabylonJS Playground Demo Link
{% endembed %}

{% hint style="info" %}
**Scene** object gets **engine** as the input argument. You don't have to worry about the engine when you are working on the playground but when you are working on your local code sample, we will create the engine as well.
{% endhint %}

### Camera

&#x20;** **_**Arc Rotate Camera**_**  **  acts like a satellite in orbit around a target and always points towards the target position. In our case, it is pointing towards the box. Where ever you move your camera, it will still point to towards the box.&#x20;

Arc Rotate Camera parameters are: **name** you want to give to your camera, **alpha**(radians) the longitudinal rotation, **beta** _beta_ (radians) the latitudinal rotation, **radius(**the distance from the target position), **target position**(center where the box will be created as a default), **scene**(optional argument). In this code example scene is not given as an argument and defaults to the scene object on the playground.&#x20;

![Arc Rotate Camera parameters: alpha, beta, radius and target position.](../../../.gitbook/assets/camalphabeta.jpg)

{% hint style="info" %}
&#x20;Setting _beta_ to **0** or **PI** can, for technical reasons, **cause problems.**
{% endhint %}

### Light

A **hemispheric light** is an easy way to simulate an ambient environment light. In our case, we are doing the bare minimum, just giving a name to the light and set it's location.

Setting y location to 1 while our main object is in the center (0,0,0) location will move the light above the object. &#x20;

### Box Mesh

We are creating a Box Mesh by calling BABYLON.MeshBuilder.CreateBox method with the minimum requirements, a name and an options empty object. &#x20;

### Exercise

* [ ] Navigate to the code sample playground: [https://playground.babylonjs.com/#KBS9I5#158](https://playground.babylonjs.com/#KBS9I5#158)
* [ ] Move your mouse over the box and click & drag.
* [ ] Uncomment line 5 and save or play the playground example.&#x20;
* [ ] Again, move mouse over the box and click & drag.
* [ ] On the BABYLON.MeshBuilder.CreateBox method replace the empty object with this object: {width: 4, height: 2}.&#x20;

### Next Steps

Continue exploring **how to create a 3D scene with other libraries**

{% content-ref url="threejs-scene.md" %}
[threejs-scene.md](threejs-scene.md)
{% endcontent-ref %}

Keep working with **BabylonJS** and **dive deeper into WebXR** on the [Babylon.js chapter](../../babylon.js/):

{% content-ref url="../../babylon.js/" %}
[babylon.js](../../babylon.js/)
{% endcontent-ref %}

Read more on [BabylonJS documentation](https://doc.babylonjs.com/):

{% embed url="https://doc.babylonjs.com/" %}



Browse [community BabylonJS demos](https://www.babylonjs.com/community/):

{% embed url="https://www.babylonjs.com/community/" %}



