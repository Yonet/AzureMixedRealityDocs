# How to make your buttons follow your hand?

MRTK uses what are known as **Solvers** to allow UI elements to follow the user or other game objects in the scene. The **Radial View** solver is a tag-along component that keeps a particular portion of a GameObject within the user's view.

You can make a button follow your hand by adding the **Radial View (Script)** component to the object.

First, drag a button prefab from **MixedRealityToolkit.SDK** > **Features** > **UX** > **Interactable** > **Prefabs** to the Hierarchy window.

![Drag button prefab to Hierarchy Window](../../../.gitbook/assets/drag_button_to_hierarchy.PNG)

In the Hierarchy window, select the button prefab. In the Inspector window, click **Add Component**. Search for **Radial View**. Once found, select to add the component to the button.

![Add Radial View (Script) Component](../../../.gitbook/assets/radial_view_script.PNG)

When you add the **Radial View (Script)** component to the button, the **Solver Handler (Script)** component is added as well because it is required by the **Radial View (Script)**.

![Solver Handler (Script) Component](../../../.gitbook/assets/solver_script.PNG)

The **Solver Handler (Script)** component needs to be configured so that the button follows the user's hand. First, change **Tracked Target Type** to **Hand Joint**. This will enable you to define which hand joint the button follows.

![Change Tracked Target Type to Hand Joint](../../../.gitbook/assets/tracked_target_type.PNG)

Next, for the **Solver Handler (Script)** component, change **Tracked Handness** to **Right**. This setting determines which hand is tracked.

![Change Handness to Right](../../../.gitbook/assets/track_handness.PNG)

There over 20 hand joints available for tracking. Still inside the **Solver Handler (Script)** component, change **Tracked Hand Joint** to **Wrist** so that the button tracks the user's wrist.

![Change Tracked Hand Joint to Wrist](../../../.gitbook/assets/tracked_hand_joint.PNG)

Now that the hand tracking is configured, you need to configure the **Radial View (Script)** component to further define where the button is located and how it is viewed in relation to the user. First, change **Reference Direction** to **Facing World Up**. This parameter determines which direction the button faces.

![Change Reference Direction to Facing World Up](../../../.gitbook/assets/reference_direction.PNG)

Next, in the **Radial View (Script)** component, change the **Min Distance** and **Max Distance** to **0**. The Min and Max Distance parameters determine how far the button should be kept from the user. As a reminder, the unit of measurement in Unity is meters. Therefore, a **Min Distance** of 1 would push the buttona way to ensure it is never closer than 1 meter to the user.

![Change Min and Max Distance](../../../.gitbook/assets/min_max_distance.PNG)

Now that the button is configured to follow your right wrist, press **Play** to enter Game mode and test the solver in the in-editor simulator. Press and hold the space bar to bring up the hand. Move the mouse cursor around to move the hand, and click and hold the left mouse button to rotate the hand:

![Use In-Editor Simulator to Test](../../../.gitbook/assets/press_play.PNG)