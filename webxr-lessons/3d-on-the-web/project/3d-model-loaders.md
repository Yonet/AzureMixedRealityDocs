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

