# How to load a 3D Model

ThreeJS

{% embed url="https://threejs.org/examples/\#webgl\_loader\_gltf" caption="ThreeJS gltf loader demo" %}

Only a few loaders \(e.g. ObjectLoader\) are included by default with three.js — others should be added to your app individually.

```typescript
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';
```

Once you've imported a loader, you're ready to add a model to your scene. Syntax varies among different loaders — when using another format, check the examples and documentation for that loader. For glTF, usage with global scripts would be:

```typescript
const loader = new GLTFLoader();

loader.load( 'path/to/model.glb', function ( gltf ) {

	scene.add( gltf.scene );

}, undefined, function ( error ) {

	console.error( error );

} );
```

See [GLTFLoader documentation](https://threejs.org/docs/index.html#examples/en/loaders/GLTFLoader) for further details.

### Troubleshooting

You've spent hours modeling an artisanal masterpiece, you load it into the webpage, and — oh no! 😭 It's distorted, miscolored, or missing entirely. Start with these troubleshooting steps:

1. Check the JavaScript console for errors, and make sure you've used an _onError_ callback when calling _.load\(\)_ to log the result.
2. View the model in another application. For glTF, drag-and-drop viewers are available for [three.js](https://gltf-viewer.donmccurdy.com/) and [babylon.js](http://sandbox.babylonjs.com/). If the model appears correctly in one or more applications, [file a bug against three.js](https://github.com/mrdoob/three.js/issues/new). If the model cannot be shown in any application, we strongly encourage filing a bug with the application used to create the model.
3. Try scaling the model up or down by a factor of 1000. Many models are scaled differently, and large models may not appear if the camera is inside the model.
4. Try to add and position a light source. The model may be hidden in the dark.
5. Look for failed texture requests in the network tab, like _C:\\Path\To\Model\texture.jpg_. Use paths relative to your model instead, such as _images/texture.jpg_ — this may require editing the model file in a text editor.

