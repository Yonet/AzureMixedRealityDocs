# How to build your project for HoloLens?

* In the Unity menu, select **File** &gt; **Build Settings...** to open the Build Settings window.

![Build settings.](../../../.gitbook/assets/buioldsettings.png)

*  In the Build Settings window, select **Universal Windows Platform** and click the **Switch Platform** button.

![Switch platform to Windows Universal Platform.](../../../.gitbook/assets/switchplatform.png)

*  Click on **Project Settings** in the **Build Settings window** or the **Unity menu**, select **Edit** &gt; **Project Settings...** to open the Project Settings window.

![Project settings.](../../../.gitbook/assets/projsettings.png)

* In the Project Settings window, select **Player** &gt; **XR Settings** to expand the XR Settings.

![ Player XR settings.](../../../.gitbook/assets/xrset.png)

*  In the XR Settings, check the **Virtual Reality Supported** checkbox to enable virtual reality, then click the **+** icon and select **Windows Mixed Reality** to add the Windows Mixed Reality SDK.

![XR settings Mixed Reality Supported checkbox.](../../../.gitbook/assets/wmrxrsettings.png)

{% hint style="info" %}
Your projects settings might have been configured by Mixed Reality Toolkit.
{% endhint %}

* Optimize the XR Settings as follows:
  * Set Windows Mixed Reality **Depth Format** to **16-bit depth.**
  * Check the Windows Mixed Reality **Enable Depth Sharing** checkbox.
  * Set Stereo **Rendering Mode\*** to **Single Pass Instanced.**

![Optimization settings for XR.](../../../.gitbook/assets/xroptimize.png)

*  In the Project Settings window, select **Player** &gt; **Publishing Settings** to expand the Publishing Settings. Scroll down to the **Capabilities** section and check the **SpatialPerception** checkbox.

![Spatial Perception enabled.](../../../.gitbook/assets/spatialperception.png)

Save your project and open up the Build Settings. Click on Build button, not Build and Run. When prompted, create a new folder\(ex:HoloLensBuild\) and select your new folder to build your files into.

{% hint style="danger" %}
Click on Build button, not Build and Run.
{% endhint %}

![Build your project into a new folder by clicking build button. ](../../../.gitbook/assets/build.png)

