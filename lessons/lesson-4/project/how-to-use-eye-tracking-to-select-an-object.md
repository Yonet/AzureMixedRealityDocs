# How to Use Eye-tracking to Select an Object

You can use eye-tracking to select objects. In this project, you will learn how to select an object using a combination of eye-gaze and either the voice command **Select** or the air-tap Select gesture. Before you begin, make sure that your project is setup for eye tracking.

In the Hierarchy window, select the object. In the Inspector window, click **Add Component** and search for the **Eye Tracking Target** script. Once found, select to add the **Eye Tracking Target (Script)** to the object.

![Add Eye Tracking Target script](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/add_eye_tracking_target.png)

Now that the **Eye Tracking Target (Script)** component has been added to the object, you need to configure the parameters to define how to select the object. First, in the **Eye Tracking Target (Script)** component, change the **Select Action** to **Select**. This defines the air-tap action for this object as **Select**.

![Assign object and action](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/select_action.png)

Next, expand **Voice Select**. Set the voice command list **Size** to 1.

![Assign object and action](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/voice_select_1.png)

A new **Element 0** appears below. Using the dropdown next to **Element 0** select **Select**. This defines the speech command action for this object as **Select**.

![Assign object and action](../../../.gitbook/assets/how-to-use-eye-tracking-to-select-an-object/element_0.png)

The object is now configured for the user to gaze and either say **Select** or use the Select air-tap gesture to select the object.