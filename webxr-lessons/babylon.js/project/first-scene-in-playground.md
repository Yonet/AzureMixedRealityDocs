# How to create your first Scene in Playground

We will create our scenes, save and share them on playground.

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
