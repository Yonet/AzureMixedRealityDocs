# How to enable VR?

There are few changes we need to make to turn our experience into a VR experience.

* [ ] Import VR button into your scene.

```typescript
import { VRButton } from "/jsm/webxr/VRButton";
```

* [ ] Enable XR on renderer.
* [ ] Append the VRButton to your html body.

```typescript
renderer.xr.enabled = true;
document.body.appendChild(VRButton.createButton(renderer));

```

* [ ] In your animate function, replace _requestAnimationFrame_ to :

  ```text
  renderer.setAnimationLoop(animate);
  ```

### Run the VR experience on your phone

If you are on an iOS



