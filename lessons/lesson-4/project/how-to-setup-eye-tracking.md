# How to setup eye-tracking

To use eye tracking in your app, you must first setup eye tracking which requires the 4 steps below:

1. Setup the scene
2. Setup MRTK profiles required for eye-tracking
3. Create an **Eye Gaze Data Provider**
4. Enable eye-tracking in the **GazeProvider (Script)**

## Setup the Scene

Configure the scene for Mixed Reality Toolkit by navigating to **Mixed Reality Toolkit** > **Add to Scene and Configure** in the Unity menu.

![Configure the scene for MRTK](../../../.gitbook/assets/how-to-setup-eye-tracking/configure_scene.png)

## Setup MRTK Profiles Required for Eye-Tracking

After the scene is configured for MRTK, choose a profile for MRTK. This profile will be modified to be configured for eye-tracking, however, the default configuration profile cannot be modified. Therefore, you must first clone the configuration profile and make changes for a new configuration profile.

In the Hierarchy window, click the **MixedRealityToolkit** object. In the Inspector window, click **Clone**.

![Clone Configuration profile](../../../.gitbook/assets/how-to-setup-eye-tracking/clone.png)

In the **Clone Profile** window, click **Clone** to create a configuration new profile.

![Clone Profile window](../../../.gitbook/assets/how-to-setup-eye-tracking/clone_profile.png)

In the Inspector window, select **Input** and click **Clone**.

![Click Clone](../../../.gitbook/assets/how-to-setup-eye-tracking/input.png)

In the **Clone Profile** window, click **Clone** to create a new Input System profile.

![Create new Input System profile](../../../.gitbook/assets/how-to-setup-eye-tracking/input_system_profile_new.png)

In the Inspector window, navigate to **Input Data Providers** > **Input Simulation Service**. Click **Clone**.

![Input Simulation Service](../../../.gitbook/assets/how-to-setup-eye-tracking/input_simulation_service.png)

In the **Clone Profile** window, click **Clone** to create a new Input Simulation Service profile.

![Create new Input Simulation Service profile](../../../.gitbook/assets/how-to-setup-eye-tracking/input_simulation_service_new.png)

In the Inspector window, within the **Input Data Providers** section, click **+ Add Data Provider**.

![Add data provider](../../../.gitbook/assets/how-to-setup-eye-tracking/add_data_provider.png)

The new data provider is added to the button of the list. 

![New data provider](../../../.gitbook/assets/how-to-setup-eye-tracking/new_data_provider.png)

xpand the new data provider. For **Type** select **Microsoft.MixedReality.Toolkit.WindowsMixedReality.Input** > **WindowsMixedRealityEyeGazeDataProvider**

![Type](../../../.gitbook/assets/how-to-setup-eye-tracking/type.png)

For **Supported Platform(s)** select **Windows Universal**

![Supported Platform(s)](../../../.gitbook/assets/how-to-setup-eye-tracking/supported_platforms.png)

## Enable Eye-Tracking in the Gaze Provider (Script)

In the Hierarchy window, select your object. In the Inspector window, click **Add Component** and search for **Gaze Provider**. Once found, add the **GazeProvider (Script)** to the object.

![Search for Gaze Provider](../../../.gitbook/assets/how-to-setup-eye-tracking/add_component.png)

In the Inspector window, scroll to the **GazeProvider (Script)** component. Check the box for **Use Eye Tracking**.

![Check Use Eye Tracking](../../../.gitbook/assets/how-to-setup-eye-tracking/use_eye_tracking.png)