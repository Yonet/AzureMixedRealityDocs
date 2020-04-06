# What is Scene Understanding?

**Scene Understanding** is an advanced **feature of Spatial Awareness** that gives **HoloLens 2** developers a structured, high-level **environment representation**.

Your mixed reality device is constantly integrating information about what it sees in your environment. Scene Understanding funnels all of these data sources and produces **one single cohesive abstraction**.

With Scene Understanding, you can rely on the system to tell you when it has detected certain **surfaces** and identify the surfaces as **walls, floors, ceilings**, and **platforms**. Scene Understanding creates a watertight mesh of your environment, even if you haven't scanned it completely.

{% hint style="danger" %}
Note that Scene Understanding SDK is only available for **HoloLens 2**.
{% endhint %}

The goal of **Scene understanding** is to **transform** the **un-structured environment sensor data** that your Mixed Reality device captures and to convert it into a powerful but abstracted representation that is intuitive and easy to develop for. [The Scene Understanding SDK](https://aka.ms/UnitySceneUnderstandingSDK) acts as the communication layer between your application and the Scene Understanding runtime. It's aimed to mimic existing standard constructs such as 3d scene graphs for 3d representations and 2D rectangles/panels for 2d applications. In general Scene Understanding is **framework agnostic** allowing for [**interoperability**](../../../glossary/#interoperability) between varied frameworks that interact with it.

![Common spatial mapping usage scenarios: placement, occlusion, physics and navigation.](../../../.gitbook/assets/sceneunderstandingusage.png)

{% hint style="info" %}
The process of converting the raw sensor data into a Scene is a potentially **expensive operation** that could take seconds for **medium spaces \(~10x10m\)** to minutes for **very large spaces \(~50x50m\)** and therefore it is not something that is being computed by the device without application **request.**
{% endhint %}

