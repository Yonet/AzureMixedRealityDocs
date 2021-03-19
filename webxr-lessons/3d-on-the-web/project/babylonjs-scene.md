---
description: Basic Scene with a cube
---

# BabylonJS Scene

We will create our Babylon.js scene on Babylon Playground. Find out more about the editor on [What is playground?](../../babylon.js/concepts/what-is-playground.md) chapter.

To create a basic Babylon.js scene, we initialize a **scene**, create **camera,** **light** and a **mesh** and return the scene object.

### BabylonJS Code

```typescript
const createScene =  () => {
    const scene = new BABYLON.Scene(engine);

    const camera = new BABYLON.ArcRotateCamera("camera", -Math.PI / 2, Math.PI / 2.5, 3, new BABYLON.Vector3(0, 0, 0));

    const light = new BABYLON.HemisphericLight("light", new BABYLON.Vector3(0, 1, 0));

    const box = BABYLON.MeshBuilder.CreateBox("box", {});

    return scene;
}
```

{% embed url="https://playground.babylonjs.com/\#KBS9I5\#158" caption="BabylonJS Playground Demo Link" %}

{% hint style="info" %}
**Scene** object gets **engine** as the input argument. You don't have to worry about the engine when you are working on the playground but when you are working on your local code sample, we will create the engine as well.
{% endhint %}

### Camera

 ****_**Arc Rotate Camera**_  ****acts like a satellite in orbit around a target and always points towards the target position. In our case, it is pointing towards the box. Where ever you move your camera, it will still point to towards the box. 

Arc Rotate Camera parameters are: **name** you want to give to your camera, **alpha**\(radians\) the longitudinal rotation, **beta** _beta_ \(radians\) the latitudinal rotation, **radius\(**the distance from the target position\), **target position**\(center where the box will be created as a default\), **scene**\(optional argument\). In this code example scene is not given as an argument and defaults to the scene object on the playground. 

![Arc Rotate Camera parameters: alpha, beta, radius and target position.](../../../.gitbook/assets/camalphabeta.jpg)

{% hint style="info" %}
 Setting _beta_ to **0** or **PI** can, for technical reasons, **cause problems.**
{% endhint %}

### Light

A **hemispheric light** is an easy way to simulate an ambient environment light. In our case, we are doing the bare minimum, just giving a name to the light and set it's location.

Setting y location to 1 while our main object is in the center \(0,0,0\) location will move the light above the object.  

### Box Mesh

We are creating a Box Mesh by calling BABYLON.MeshBuilder.CreateBox method with the minimum requirements, a name and an options empty object.  

### Exercise

* [ ] Navigate to the code sample playground: [https://playground.babylonjs.com/\#KBS9I5\#158](https://playground.babylonjs.com/#KBS9I5#158)
* [ ] Move your mouse over the box and click & drag.
* [ ] Uncomment line 5 and save or play the playground example. 
* [ ] Again, move mouse over the box and click & drag.
* [ ] On the BABYLON.MeshBuilder.CreateBox method replace the empty object with this object: {width: 4, height: 2}. 

### Next Steps

Learn more about Babylon.js on the [Babylon.js chapter](../../babylon.js/):

{% page-ref page="../../babylon.js/" %}

Read more on [babylon.js documentation](https://doc.babylonjs.com/):

{% embed url="https://doc.babylonjs.com/" %}



Browse [community babylon.js demos](https://www.babylonjs.com/community/):

{% embed url="https://www.babylonjs.com/community/" %}





