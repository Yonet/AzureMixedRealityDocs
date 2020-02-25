# How to Add Button Prefabs to Your Project

Mixed Reality Toolkit is equipped with a variety of button prefabs that you could add to your project. A prefab is a pre-configured GameObject stored as a Unity Asset and can be reused throughout your project.

You can find button prefabs available in MRTK by navigating to **MixedRealityToolkit.SDK** > **Features** > **UX** > **Interactable** > **Prefabs**.

[insert picture]

In this project, you will learn how to change the color of a cube when a button is pressed.

First, select the button of your choice from the Project window and drag into the Hierarchy window.

[insert picture]

Change the button's **Transform Position** so that it's positioned in front of the camera to x = 0, y = 0, and z = 0.5

[insert picture]

Next, right click on an empty spot in the Hierarchy window and click **3D Object** > **Cube**. 

[insert picture]

With the Cube object still selected, in the Inspector window, change the **Transform Position** so that the cube is located near but not overlapping the button. In addition, resize the cube by changing the **Transform Scale**.

[insert picture]

In the Hierarchy window, select the button. In the Inspector window, navigate to the **Interactable (Script)** component.

[insert picture]

In the **Events** section, expand the **Receivers** section.

[insert picture]

Click the **Add Event** button to create a new event receiver of **Event Receiver Type** **InteractableOnPressReceiver**.

[insert picture]

For the newly created **InteractableOnPressReceiver** event, change the **Interaction Filter** to **Near and Far**.

[insert picture]

From the Hierarchy window, click and drag the **Cube** GameObject into the **Event Properties** object field for the **On Press()** event to assign the Cube as a receiver of the On Press () event.

[insert picture]

Next, click the action dropdown (currently assigned **No Function**) and select **MeshRenderer** > **Material material**. This action will set the Cube's material property to change when the button is pressed.

[insert picture]

Now, assign a color for the Cube to change to when the button is pressed. Click the small **circle** icon next to the **Material** field (currently assigned **None (Material)**) to open the **Select Material** window.

[insert picture]

MRTK provides a variety of materials that can be used in your projects. In the search bar, search for **MRTK_Standard** and select your color of choice.

[insert picture]

Now that the event is configured for when the button is pressed, you now need to configure an event that occurs when the button is released. For the **On Release ()** event, click and drag the **Cube** GameObject into the **Event Properties**.

[insert picture]

Next, click the action dropdown (currently assigned **No Function**) and select **MeshRenderer** > **Material material**. This action will set the Cube's material property to change when the button is released.

[insert picture]

Now, assign a color for the Cube to change to when the button is released. Click the small circle icon next to the Material field (currently assigned None (Material)) to open the Select Material window and search for **MRTK_Standard**. Select your choice of color.

[insert picture]

Now that both the On Press () and On Trigger () events are configured for the button, press **Play** to enter Game mode and test the button in the in-editor simulator.

To press the button, press the spacebar + mouse scroll forward.

[insert picture]

To release the button, press the spacebar + mouse scroll backward.

[insert picture]