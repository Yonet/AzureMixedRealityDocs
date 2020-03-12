# How to get started with Unity?

## What is Unity?

[Unity](https://unity.com/) is a platform, often referred to as an *engine*, that can be used to develop mixed reality applications. The benefit of using such a platform is that Unity has various built-in functionality which can help developers bring their ideas to life faster as opposed to starting from scratch.

Although this lesson covers basic functionality for developing a mixed reality application in Unity, we recommend taking some time to explore the tutorials provided on [Unity Learn](https://unity3d.com/learn/tutorials) for further guidance.

In addition to tutorials on Unity Learn, Unity provides a [manual](https://docs.unity3d.com/Manual/index.html) to help you learn how to use the editor. Furthermore, the [Unity Scripting Reference](https://docs.unity3d.com/ScriptReference/index.html) contains details of the scripting API that Unity provides.

## Download Unity Hub

The [Unity Hub](https://docs.unity3d.com/Manual/GettingStartedUnityHub.html) is a management tool that you can use to manage all of your Unity Projects and installations. Unity Hub is great for managing multiple installations of the Unity Editor along with their associated components, creating new Projects, and opening existing Projects. Before you install Unity Hub, ensure that your pc meets the [system requirements](https://docs.unity3d.com/Manual/system-requirements.html) for Unity.

On the [Download Unity](https://unity3d.com/get-unity/download) page, select **Download Unity Hub** to download the application and begin the installation process.

To install and use the Unity Editor, you must have a Unity Developer Network (UDN) account. If you already have an account, sign in, choose your licenses type, and proceed to the Installing the Unity Editor section.

If you do not have an account, follow the prompts to create one. You can choose to create a Unity ID or use one of the social sign-ins.

Once the Unity Hub installation is complete, launch the Unity Hub.
There are 3 tabs within the Unity Hub. A description of what each tab entails is provided below:

|Tab  |Description  |
|---------|---------|
|Projects    |  On this tab, you can view all projects created from or added to the Unity Hub. To create a new project, either click **New** ( which selects the latest version of Unity by default) **or** click the drop down arrow next to New which enables you to select the version of Unity to use for the project.<br><br>If you have a Unity project saved to your computer, you can manually add the project to Unity Hub using the **Add** button. Once clicked, a file explorer window appears which enables you to navigate to the location of the file to add to Unity Hub.     |
|Learn     |   On this tab, you can find resources from Unity Learn in the form of projects o)r tutorials. Selecting a project from the **Project** tab provides you with the option to either download the project files and work through a guided tutorial in Unity **or** visit the webpage for the tutorial on Unity Learn. Selecting a tutorial from the **Tutorials** tab provides you with a link to visit the webpage for the tutorial on Unity Learn.  |
|Installs     |    On this tab, you can view all current installations of Unity as well as the respective version and modules (also referred to as *components*). If you need to install additional modules for an installed version of Unity, click the 3 vertical dots and select **Add Modules**. A list of available modules will display in which you could select and download for the respective version of Unity.<br><br>You could also install additional versions of Unity using the **Add** button. Unity Hub provides you with a list of the **Latest Official Releaes** and **Latest Pre-Releases**. When installing a version of Unity in the Unity Hub, you are prompted to first select the version followed by the modules to install for the respective version of Unity. If you are in need of an older version of Unity, visit the [Unity Download Archive](https://unity3d.com/get-unity/download/archive) to locate the desired version. Once you locate the desired version in the Unity Download Archive, select **Unity Hub** which enables you to complete the download and installation from the Unity Hub.<br><br>If you have a Unity download saved to your computer, you can manually add the Unity version to Unity Hub using the **Locate** button. Once clicked, a file explorer window appears which enables you to navigate to the location of the file to begin the installation.

## Install Unity

To complete this lesson, you will need to install a Unity version appropriate for your device. For HoloLens 1 development, you will need to install Unity version 2018.4 LTS. For all other devices, you will need to install Unity version 2019.2.X.

**Hololens (1st gen)**

If you are developing for a HoloLens 1, you will need to access version 2018.4 LTS via the [Long Term Support Releases](https://unity3d.com/unity/qa/lts-releases). Select **Unity Hub** next to the latest Unity 2018.4 Expand **LTS Release 2018.4.17f1** and select **Download (Win)** under **Unity Editor Download Assistant**.

![Download Unity LTS Release 2018.4.17f1](../../../.gitbook/assets/unity_v2018.png)  

The installation wizard will walk you through the steps to install this version of Unity. During installation, you will be prompted to select workloads to install. Select **Universal Windows Platform Build Support**. This platform is only available for use if you're using Unity on a Windows computer.

You could later add this version of Unity to the Unity Hub by using the **Installs** section and **Locate** the download.

**HoloLens 2 and other devices**

Navigate to the **Installs** tab and click **Add**.

![Unity Installs](../../../.gitbook/assets/unity_installs_add.png)

**Select a version of Unity**, select the latest Unity version that starts with **2019.2** and click **Next**.

![Select Unity Version 2019.2](../../../.gitbook/assets/select_unity_version.png)

For **Add modules to your install**, you have the opportunity to select additional components to install with Unity. Under the **Platforms** section, select **Universal Windows Platform Build Support**. This platform is only available for use if you're using Unity on a Windows computer.

![Select Unity Modules](../../../.gitbook/assets/unity_modules.png)

**Documentation** is already pre-selected and can remain selected. This provides offline documentation which can be accessed in the Unity Editor via **Help** > **Scripting Reference** *or* **Help** > **Unity Manual**. The installed documentation could also be accessed on your computer by navigating to **C:\Program Files\Unity\Hub\Editor\SELECT A UNITY VERSION\Editor\Data\Documentation**).

After you've selected the necessary modules, select **Done** to begin installation.

## Create a New Unity 3D Project

Now that Unity is installed, you can create a new project using that version. In the Unity Hub, navigate to the **Projects** tab and click **New**. If you have multiple versions of Unity installed, click the drop down arrow next to **New** and select a version that is 2019.2.X.

Enter a **Project Name** for your project and select a **Location** to save the project. When working on Windows, there is a MAX_PATH limit of 255 characters. Unity is affected by these limits and may fail to compile if any file path is longer than 255 characters. Consequently, it is strongly recommended to store your Unity project as close to the root of the drive as possible.

![Create new Unity project](../../../.gitbook/assets/create_project.png)

Click **Create** to create the project. Once the project has been created, the Unity Editor will launch.