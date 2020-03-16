# How to use eye-tracking to manipulate an object

Eye-tracking can be used to manipulate objects by creating an event to trigger an action. In this project, you will learn how to rotate an object while looking at the object. Before you begin, make sure that your project is setup for eye tracking.

In the Hierarchy window, select the object. In the Inspector window, click **Add Component** and search for the **Eye Tracking Target** script. Once found, select to add the **Eye Tracking Target (Script)** to the object.

![Add Eye Tracking Target script](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/add_eye_tracking_target.png)

With the object still selected, click **Add Component** and search for the **Eye Tracking Tutorial Demo** script. Once found, select to add the **Eye Tracking Tutorial Demo (Script)** to the object.

![Add Eye Tutorial Demo script](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/add_eye_tracking_tutorial_demo.png)

Now that the **Eye Tracking Tutorial Demo (Script)** has been added to the object, you need to create an event in the **Eye Tracking Target (Script)** component that triggers the object to rotate while the user is looking at the object. In the **Eye Tracking Target (Script)** component, create a new **While Looking At Target ()** event.

![Create a new While Looking At Target event](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/while_looking_at.png)

Next, assign the object to the event. Then, select **EyeTrackingTutorialDemo.RotateTarget** as the action to be triggered.

![Assign object and action to the event](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/assign_action.png)

You can test this interaction using the in-editor simulation. Press play to enter Game mode. The in-editor simulation uses the position of the camera as the location of the user's eyes. Using the **A** or **D** keys on the keyboard, move the camera to the left or right of the object. As you move the camera, the object is no longer the focus and therefore stops rotating.

![Object rotate in Game mode](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/play.png)