# Basic A-Frame Scene

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://aframe.io/releases/1.3.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  </body>
</html>
```

Primitives are similar to [prefabs in Unity](https://docs.unity3d.com/Manual/Prefabs.html). They abstract the core entity-component API to:

* Pre-compose useful components together with prescribed defaults
* Act as a shorthand for complex-but-common types of entities (e.g., `<a-sky>`)
* Provide a familiar interface for beginners since A-Frame takes HTML in a new direction

You can see the resulting page on Glitch

{% embed url="https://glitch.com/~aframe" %}
Basic Aframe scene on Glitch
{% endembed %}
