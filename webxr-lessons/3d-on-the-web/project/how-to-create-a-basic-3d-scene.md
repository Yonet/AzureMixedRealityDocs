# How to create a basic 3D scene?

To create a basic scene we need to initialize a **scene** object. You can think of a **scene** as a **stage** that will hold your production. Everything that will be visible to the viewer will be added to the scene.

![A scene is an object that holds everything you will display](../../../.gitbook/assets/2019-09-02\_1246-660x400.png)

We need to add a **camera** object to the scene that will be our viewers perspective. Anything on the scene but not in the view of the camera won't be visible on your canvas.&#x20;

![Camera is essential for rendering your scene to canvas](../../../.gitbook/assets/professional-video-camera-high-definition-video-camcorder-png-favpng-deeud9gbwkfw1f1ge4pmnzpr6.jpg)

We also need a **light** source for our objects to be visible.&#x20;

![Without the lights, we will render only black to the canvas.](../../../.gitbook/assets/kisspng-stage-lighting-fresnel-lantern-light-emitting-diod-stage-light-5abfe733c8a9c2.4839009215225260038219.jpg)

Finally, we will create a basic shape(**mesh**), box.&#x20;

![Box Mesh to be rendered](../../../.gitbook/assets/boxmesh.png)

![Geometry vs Material of a mesh](../../../.gitbook/assets/vertex.png)

{% embed url="https://threejs.org/examples/#webgl_multiple_scenes_comparison" %}
ThreeJS Mesh = material + geometry example
{% endembed %}



Let's create the basic scene using different libraries.
