# How to add button prefabs to your project?

## How to add button prefabs to your project?

Mixed Reality Toolkit is equipped with a variety of button prefabs that you could add to your project. A prefab is a pre-configured GameObject stored as a Unity Asset and can be reused throughout your project.

You can find button prefabs available in MRTK by navigating to **MixedRealityToolkit.SDK** &gt; **Features** &gt; **UX** &gt; **Interactable** &gt; **Prefabs**.

![MRTK Button Prefabs](../../../.gitbook/assets/button_prefabs.png)

In this project, you will learn how to change the color of a cube when a button is pressed.

First, select the button of your choice from the Project window and drag into the Hierarchy window.

![Drag button prefab to Hiearchy window](../../../.gitbook/assets/drag_button_to_hierarchy.png)

Change the button's **Transform Position** so that it's positioned in front of the camera to x = 0, y = 0, and z = 0.5

![Change Cube Transform Position](../../../.gitbook/assets/button_transform_position.png)

Next, right click on an empty spot in the Hierarchy window and click **3D Object** &gt; **Cube**.

![Create Cube](../../../.gitbook/assets/create_cube.png)

With the Cube object still selected, in the Inspector window, change the **Transform Position** so that the cube is located near but not overlapping the button. In addition, resize the cube by changing the **Transform Scale**.

![Change Transform properties](../../../.gitbook/assets/transform_cube.png)

In the Hierarchy window, select the button. In the Inspector window, navigate to the **Interactable \(Script\)** component.

![Interactable \(Script\) component](../../../.gitbook/assets/interactable_script_component.png)

In the **Events** section, expand the **Receivers** section.

![Expand Receivers section](../../../.gitbook/assets/expand_events_receivers.png)

Click the **Add Event** button to create a new event receiver of **Event Receiver Type** **InteractableOnPressReceiver**.

![Create a new event receiver](../../../.gitbook/assets/interactableonpressreceiver_new.png)

For the newly created **InteractableOnPressReceiver** event, change the **Interaction Filter** to **Near and Far**.

![Change Interaction Filter to Near and Far](../../../.gitbook/assets/near_and_far.png)

From the Hierarchy window, click and drag the **Cube** GameObject into the **Event Properties** object field for the **On Press\(\)** event to assign the Cube as a receiver of the On Press \(\) event.

![Assign Cube GameObject](../../../.gitbook/assets/cube_receiver.png)

Next, click the action dropdown \(currently assigned **No Function**\) and select **MeshRenderer** &gt; **Material material**. This action will set the Cube's material property to change when the button is pressed.

![Assign Material material](../../../.gitbook/assets/material_material.png)

Now, assign a color for the Cube to change to when the button is pressed. Click the small **circle** icon next to the **Material** field \(currently assigned **None \(Material\)**\) to open the **Select Material** window.

![Assign Pressed color](../../../.gitbook/assets/select_material.png)

MRTK provides a variety of materials that can be used in your projects. In the search bar, search for **MRTK\_Standard** and select your color of choice.

![Search for MRTK\_Standard](../../../.gitbook/assets/search_mrtk_standard.png)

Now that the event is configured for when the button is pressed, you now need to configure an event that occurs when the button is released. For the **On Release \(\)** event, click and drag the **Cube** GameObject into the **Event Properties**.

![Assign Cube GameObject](../../../.gitbook/assets/on_release_assign_cube.png)

Next, click the action dropdown \(currently assigned **No Function**\) and select **MeshRenderer** &gt; **Material material**. This action will set the Cube's material property to change when the button is released.

![Assign Material material](../../../.gitbook/assets/on_release_material_material.png)

Now, assign a color for the Cube to change to when the button is released. Click the small circle icon next to the Material field \(currently assigned None \(Material\)\) to open the Select Material window and search for **MRTK\_Standard**. Select your choice of color.

![Assign Release color](../../../.gitbook/assets/on_release_color.png)

Now that both the On Press \(\) and On Trigger \(\) events are configured for the button, press **Play** to enter Game mode and test the button in the in-editor simulator.

To press the button, press the space bar + mouse scroll forward.

![Press button](../../../.gitbook/assets/button_pressed_magenta.png)

To release the button, press the space bar + mouse scroll backward.

![Release button](../../../.gitbook/assets/button_release_green.png)

