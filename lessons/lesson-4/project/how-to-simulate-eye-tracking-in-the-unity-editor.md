# How to Simulate Eye-Tracking in the Unity Editor

You can simulate eye-tracking in the Unity Editor by enabling simulated eye tracking. The eye gaze signal is simulated by using the camera's location as eye gaze origin and the camera's forward vector as eye gaze direction. 

Setting up eye-tracking simulation requires changing the MRTK configuration profile, however, the default configuration profile cannot be modified. Therefore, you must first clone the configuration profile and make changes for a new configuration profile.

In the Hierarchy window, click the **MixedRealityToolkit** object. In the Inspector window, click **Clone**.

![Clone Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/clone_configuration_profile.png)

In the **Clone Profile** window, click **Clone** to create a configuration new profile.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/new_profile.png)

In the Inspector window, select **Input** and click **Clone**.

![Clone Input profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/input_clone.png)

In the **Clone Profile** window, click **Clone** to create a new Input System profile.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/new_input_profile.png)

In the Inspector window, navigate to **Input Data Providers** > **Input Simulation Service**.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/input_data_providers.png)

Click **Clone**.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/simulation_service_clone.png)

In the **Clone Profile** window, click **Clone** to create a new Input Simulation Service profile.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/new_sim_service_clone.png)

In the Inspector window,inside the **Input Simulation Service**, check the **Simulate Eye Position** checkbox.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/simulate_eye_position.png)

It is recommended to avoid showing an eye gaze cursor. However, if the cursor must be visible, it's recommended to make the cursor very subtle. To hide the default head gaze cursor that is attached to the MRTK gaze point profile by default, first navigate to **Input** > **Pointers** in the Inspector window.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/pointers.png)

Click **Clone**.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/pointers_clone.png)

In the **Clone Profile** window, click **Clone** to create a new Pointer profile.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/pointer_profile_new.png)

In the **Gaze Settings** section, assign an invisible cursor prefab to the **GazeCursor**. If you downloaded the MRTK Examples folder, you can reference the included **EyeGazeCursor** prefab.

To assign the **EyeGazeCursor** prefab, first click the circle next to the **Gaze Cursor**.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/gaze_cursor.png)

In the **Select GameObject** window, search for **EyeGazeCursor**. Once found, select the prefab to assign as the **Gaze Cursor**.

![Create new Configuration profile](../../../.gitbook/assets/how-to-simulate-eye-tracking-in-the-unity-editor/search_eyegazecursor.png)