# What could go wrong?

### What are the downsides of using Blueprints instead of writing C++?

* **C++** is always **faster**. Blueprints use **Virtual Machine**\(**VM\)** to translate functionality to C++.
* If you have a Blueprint that's doing a lot of operations and complex **math every tick**\(frame rendered\), you might want to consider using native C++ functions instead.
* Blueprints are a set of functionality that is made available to you in the visual editor. You can write anything that is not available to you as Blueprints, using C++.
* Blueprints use object references, it is possible to have a circular dependency in your blueprint code.



