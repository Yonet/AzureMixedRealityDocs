# What is an Arc Camera?

_**Arc Rotate Camera**_**  **  acts like a satellite in orbit around a target and always points towards the target position. In our case, it is pointing towards the box. Where ever you move your camera, it will still point to towards the box.&#x20;

Arc Rotate Camera parameters are: **name** you want to give to your camera, **alpha**(radians) the longitudinal rotation, **beta** _beta_ (radians) the latitudinal rotation, **radius(**the distance from the target position), **target position**(center where the box will be created as a default), **scene**(optional argument). In this code example scene is not given as an argument and defaults to the scene object on the playground.&#x20;

![Arc Rotate Camera parameters: alpha, beta, radius and target position.](../../../.gitbook/assets/camalphabeta.jpg)

{% hint style="info" %}
&#x20;Setting _beta_ to **0** or **PI** can, for technical reasons, **cause problems.**
{% endhint %}
