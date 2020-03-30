# What are SceneQuads?

**SceneQuads** are computed **2D primitives** that describe **a flat surface** and has an **API** designed to be used to help **placement of the objects**. 

When using the **triangle mesh** from **Spatial Map** to perform placement, one had to scan all areas of the quad and perform **hole filling/post-processing** to identify good locations for object placement. This is not always necessary with Quads, as the Scene understanding runtime is capable of inferring which areas of the quad that were not scanned, and **invalidate areas of the quad that are not part of the surface**.

{% hint style="danger" %}
Note that Scene Understanding SDK is only available for **HoloLens 2**.
{% endhint %}

![SceneQuads with inference disabled, capturing placement areas for scanned regions. ](../../../.gitbook/assets/suquads.png)

![Quads with inference enabled, placement is no longer limited to scanned areas.](../../../.gitbook/assets/suwatertight.png)

 If your application intends to place **2D** or **3D holograms** on **rigid structures** of your environment, the simplicity and convenience of SceneQuads for placement is preferable to computing this information from the spatial mapping mesh.

