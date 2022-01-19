# Babylon.js AR scene

```javascript
import { Engine } from "@babylonjs/core/Engines/engine";
import { Scene } from "@babylonjs/core/scene";
import { FreeCamera, WebXRHitTest } from '@babylonjs/core';

import { ArcRotateCamera } from "@babylonjs/core/Cameras/arcRotateCamera";
import { Quaternion, Vector3 } from "@babylonjs/core/Maths/math.vector";
import { HemisphericLight } from "@babylonjs/core/Lights/hemisphericLight";
import { StandardMaterial } from "@babylonjs/core";
import { CreateSceneClass } from "../createScene";

import { getTokenOrRefresh } from "../utils/token_util";
import { ResultReason } from "microsoft-cognitiveservices-speech-sdk";

// If you don't need the standard material you will still need to import it since the scene requires it.
// import "@babylonjs/core/Materials/standardMaterial";
import { Texture } from "@babylonjs/core";

import grassTextureUrl from "../../assets/grass.jpg";
import { Mesh, MeshBuilder } from "@babylonjs/core/Meshes";

export class DefaultSceneWithTexture implements CreateSceneClass {

    createScene = async (
        engine: Engine,
        canvas: HTMLCanvasElement
    ): Promise<Scene> => {
        // This creates a basic Babylon Scene object (non-mesh)
        const scene = new Scene(engine);

        // This creates and positions a free camera (non-mesh)
        const camera = new FreeCamera("camera1", new Vector3(0, 1, -5), scene);

        // This targets the camera to scene origin
        camera.setTarget(Vector3.Zero());

        // This attaches the camera to the canvas
        camera.attachControl(canvas, true);

        // This creates a light, aiming 0,1,0 - to the sky (non-mesh)
        const light = new HemisphericLight("light", new Vector3(0, 1, 0), scene);

        // Default intensity is 1. Let's dim the light a small amount
        light.intensity = 0.7;

        // Our built-in 'sphere' shape.
        const sphere = Mesh.CreateSphere(
            "sphere", 32, 2,
            scene
        );

        // Move the sphere upward 1/2 its height
        sphere.position.y = 2;
        sphere.position.z = 5;

        // Load a texture to be used as the ground material
        const groundMaterial = new StandardMaterial("ground material", scene);
        groundMaterial.diffuseTexture = new Texture(grassTextureUrl, scene);

        // ground.material = groundMaterial;
        // eslint-disable-next-line @typescript-eslint/no-unused-vars
        const xr = await scene.createDefaultXRExperienceAsync({
            // ask for an ar-session
            uiOptions: {
                sessionMode: "immersive-ar",
                referenceSpaceType: "local-floor"
            },
            optionalFeatures: true,
        });

        const featuresManager = xr.baseExperience.featuresManager;


        const marker = MeshBuilder.CreateTorus("marker", { diameter: 0.1, thickness: 0.05 }, scene);
        marker.rotationQuaternion = new Quaternion();


        return scene;
    };
}

export default new DefaultSceneWithTexture();
```
