# How to enable AR and Hit-test?

Similar to VR experience, you can add AR Button to enable AR experiences. Additionally, you can specify the required and optional AR features your experience will use.

```typescript
import { ARButton } from "/jsm/webxr/ARButton";

document.body.appendChild(ARButton.createButton(renderer, { requiredFeatures: ["hit-test"] }));
```

Add a controller:  Returns a Group representing the so called **target ray** space of the controller. Use this space for visualizing 3D objects that support the user in pointing tasks like UI interaction.

```typescript
	controller = renderer.xr.getController(0);
	controller.addEventListener("select", onSelect);
	scene.add(controller);
```

When we are hitting a surface, to indicate the surface, we will create a reticle to our scene.

```typescript
	//Hit-test indicator
	reticle = new Mesh(new RingBufferGeometry(0.15, 0.2, 32).rotateX(-Math.PI / 2), new MeshBasicMaterial());
	reticle.matrixAutoUpdate = false;
	reticle.visible = false;
	scene.add(reticle);
```

Let's define the onSelect event that we attached to controller. When the select event happen, meaning user decides to place the object and we create it on the chosen location.

```typescript
function onSelect() {
	if (reticle.visible) {
		const mesh = new Mesh(geometry, phongMaterial);
		mesh.position.setFromMatrixPosition(reticle.matrix);
		mesh.scale.y = Math.random() * 2 + 1;
		scene.add(mesh);
	}
}
```

Finally in our render function, we will check in every XRFrame if we have an hit-test source to display the reticle on the surface. 

```typescript
function render(timestamp: number, frame: any) {
	if (frame) {
		earth.visible = false;
		const referenceSpace = renderer.xr.getReferenceSpace();
		const session = renderer.xr.getSession();
		if (hitTestSourceRequested === false) {
			session.requestReferenceSpace("viewer").then((referenceSpace) => {
				session.requestHitTestSource({ space: referenceSpace }).then((source) => {
					hitTestSource = source;
				});
			});

			session.addEventListener("end", () => {
				hitTestSourceRequested = false;
				hitTestSource = null;
			});
			hitTestSourceRequested = true;
		}
		if (hitTestSource) {
			const hitTestResults = frame.getHitTestResults(hitTestSource);
			if (hitTestResults.length) {
				const hit = hitTestResults[0];
				reticle.visible = true;
				reticle.matrix.fromArray(hit.getPose(referenceSpace).transform.matrix);
			} else {
				reticle.visible = false;
			}
		}
	}
	renderer.render(scene, camera);
}

```

To run the code on your device, you have to give access to your camera when prompted.

