---
description: AFrame declarative way to create a 3D scene
---

# AFrame Scene

[AFrame](https://aframe.io), simplifies creating a 3D scene by giving us a way to define our scene as html elements. Under the hood AFrame uses Three.js to do the same thing but allows you to change elements through attributes.&#x20;

{% embed url="https://glitch.com/edit/#!/aframe?path=index.html%3A17%3A7" %}
AFrame code sample link on Glitch
{% endembed %}

```
  <body>
    <a-scene background="color: #FAFAFA">
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9" shadow></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E" shadow></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D" shadow></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4" shadow></a-plane>
    </a-scene>
  </body>
```

With a frame you can create a scene using \<a-scene> html tag and nest the objects tags inside the scene. As a person who is used to working with Canvas and JavaScript, this is confusing to me but I can see why it is easier for some.&#x20;

Good news is, you can use Three.js to further create interactions for your AFrame scenes.&#x20;
