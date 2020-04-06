# What is Spatial Mapping?

**Spatial Awareness** is one of the core features of **HoloLens**. It allows the device to understand the **real world** around you.

  
The Spatial Awareness system builds a collection of **meshes that represent the shapes** in your environment, allowing developers to make some very cool interactions between holograms and real-world objects.

  
The most common **use case** is for **placing Holograms on surfaces**. If we ignore the room surfaces we can get some strange results where Holograms are behind a wall or go through physical objects. This is bad for a few reasons:

*  This is very uncomfortable for users because their eyes are constantly fighting to focus between the real surface and the Hologram.
* And second, it breaks the illusion of our 3D objects being placed in the real world.  What we recommend is to use spatial awareness to place holograms on top of a surface, or attached to a surface. If we enable spatial mapping in our apps we can place holograms in a more natural way, but if we use scene understanding you can achieve even better results, but I'll dive into that in a minute.  Make scanning a part of your experience! Even though HoloLens is constantly scanning your environment, make sure that your app has enough spatial information in order for it to be a great experience. So incorporate scanning moments into the flow of your app. These moments can be disguised by asking the user to move around an object or to look in certain a direction, but always remember to keep it short and fun.  Now back to Scene Understanding... If you use Scene Understanding in your apps, you can create magical moments where holograms are automatically placed in your room. For example, you could place a holographic screen on a wall, or even better, sit a virtual character on a user's real sofa!  On HoloLens you can download room data from the device to your PC. This allows you to import the room data as a 3d model into Unity and other development tools, and simulate the user's environments. But most importantly, you can test your spatially aware app in different settings and make tweaks to the model inside the editor.  Whenever you spawn objects in your apps, make sure that their positions respect the room's bounds. Spawning visible objects behind a real wall is a bad idea, especially if you are using spatial mapping with an occlusion shader! The Occlusion shader will hide the object since it is behind a real one. So Always check that spawned object stays within the bounds of your room. Constantly showing the spatial mesh in your app, despite looking cool, can be very noisy and distracting for the user. That's why we recommend showing the mesh only if the user needs to know that it's there, and even in those cases, pulses should be used so that their appearance is subtle and elegant. Our research has taught us that users expect holograms to behave like real objects.For example, users stay away from holograms with sharp edges and they avoid walking through holograms. Makes sure that your holograms respect their surroundings because your users will expect them to. In this chapter we've explained some fundamental recommendations around Spatially Aware apps: \* Use Scene Understanding to place objects on specific surfaces. \(Use SU for hologram placement\)
* Make scanning a part of your user experience \("Scanning part of UX"\)
* Test your app in different environments by importing mesh data into your development tool.
* Spawn objects within the room bounds.
* Only show the spatial mesh when needed. 

AND

* Make holograms respect their surroundings.

  
  
Spatially aware apps can be incredibly powerful, and if they're designed properly they can truly blend holograms with reality.  
  


