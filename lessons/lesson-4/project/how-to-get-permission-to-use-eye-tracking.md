# How to get permission to use eye-tracking

For eye-tracking capable applications, the user needs to grant app permission to use eye tracking information. You must first enable the **GazeInput** capability. MRTK provides a way to automatically enable the **GazeInput** capability.

In the Unity menu, navigate to **Mixed Reality Toolkit** > **Utilities** > **Build Window**.

![**MRTK Build Window**](../../../.gitbook/assets/how-to-get-permission-to-use-eye-tracking/mrtk_build_window.png)

In the **Build Window**, click on the **Appx Build Options** tab.

![Click Apx Build Options tab](../../../.gitbook/assets/how-to-get-permission-to-use-eye-tracking/appx_build_options.png)

Check the box next to **GazeInput**.

![Check GazeInput](../../../.gitbook/assets/how-to-get-permission-to-use-eye-tracking/gaze_input_capability.png)

This tooling will find the AppX manifest after the Unity build is completed and manually add the GazeInput capability. This tooling is **NOT** active when using Unity's built-in Build Window (i.e. **File** > **Build Settings**). When using Unity's build window, the capability will need to be manually added after the Unity build.

When starting the app on a device for the first time, a prompt should pop up asking the user for permission to use eye tracking. If it is not showing up, then that is usually an indication that the **GazeInput** capability was not set.

After the permission prompt shows once, it will not show up automatically again. 

If you are using a HoloLens 2, you can reset the eye tracking permission by going to **Settings** > **Privacy** > **Apps**.