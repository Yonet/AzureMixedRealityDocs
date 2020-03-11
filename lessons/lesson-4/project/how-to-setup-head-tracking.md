# How to setup head tracking

The **Main Camera** object tracks the movement of the user's head. You can think of the starting position of the user as x = 0, y = 0, z = 0. When you add and configure **Mixed Reality Toolkit** to your scene, the **Main Camera** object is set at the user's starting position of x = 0, y = 0, z = 0.

Although this is the default position of the **Main Camera** for MRTK, you can view this by expanding the **MixedRealityPlayspace** object in the Hierarchy window and then select the **Main Camera** object.

![Main Camera GameObject](../../../.gitbook/assets/how-to-setup-head-tracking/main_camera_object.png)

In the Inspector window, you will see that the **Transform Position** is x = 0, y = 0, z = 0.

![Main Camera Transform Position](../../../.gitbook/assets/how-to-setup-head-tracking/main_camera_position.png)