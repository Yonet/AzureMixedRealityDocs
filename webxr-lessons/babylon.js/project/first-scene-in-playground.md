# First Scene in Playground

Playground is an online editor that you can write your code and view the results. We will create our scenes, save and share them on playground.

### BabylonJS Code

First we will setup our scene with a camera, light and a basic 3D object. 

```typescript
const scene = new BABYLON.Scene(engine);
//
const camera = new BABYLON.ArcRotateCamera("camera", -Math.PI / 2, Math.PI / 2.5, 3, new BABYLON.Vector3(0, 0, 0), scene);
camera.attachControl(canvas, true);
const light = new BABYLON.HemisphericLight("light", new BABYLON.Vector3(0, 1, 0), scene);
const box = BABYLON.MeshBuilder.CreateBox("box", {}, scene);
```

{% embed url="https://playground.babylonjs.com/\#KBS9I5" caption="Basic scene with a cube on playground editor" %}

```typescript
const scene = new BABYLON.Scene(engine);
const camera = new BABYLON.ArcRotateCamera("camera", -Math.PI / 2, Math.PI / 2.5, 3, new BABYLON.Vector3(0, 0, 0), scene);
camera.attachControl(canvas, true);
const light = new BABYLON.HemisphericLight("light", new BABYLON.Vector3(0, 1, 0), scene);
const box = BABYLON.MeshBuilder.CreateBox("box", {}, scene);
```

