# How to Setup Your PC for Mixed Reality Development

## Minimum PC Hardware Guidelines

For the best experience with Windows Mixed Reality you want to start with a new Windows Mixed Reality-ready PC or a Windows Mixed Reality-compatible PC that can provide Windows Mixed Reality Ultra experiences. Windows Mixed Reality Ultra provides crisper visuals at higher refresh rates, more apps and experiences including the most graphics-intensive games, mirroring of your Windows Mixed Reality experience on your desktop and the ability to record and share (photo and video) your experiences with others.

To see if your PC can run Windows Mixed Reality run the [Mixed Reality Portal App](https://www.microsoft.com/store/apps/9NG1H8B3ZC7M).

![Mixed Reality Portal App](../../../.gitbook/assets/mr_portal_app_main.png)

After running the app, you will receive an analysis of your PC against the required hardware, drivers, and operating system. One of the following messages will display at the top of the analysis: 

- **You're good to go.** Your PC has what it takes to run Windows Mixed Reality.
- **Supports some features.** This PC may be able to run Windows Mixed Reality, but some features might be limited.
- **Can't run mixed reality.** This PC doesn't meet the minimum requirements needed to run Windows Mixed Reality.

Below the message, an evaluation is provided for your PC's hardware, drivers and operating system.

![Mixed Reality Portal App Results](../../../.gitbook/assets/mr_portal_app.png)

|Icon  |Description  |
|---------|---------|
|![Pass](../../../.gitbook/assets/check_mark.png)     |   Your PC passes the required item.      |
|![Issues](../../../.gitbook/assets/issues.png)     |   There may be issues with your PC for the given requirement. If you encounter issues, you may need to troubleshoot or upgrade your PC.     |
|![Fail](../../../.gitbook/assets/doesnt_meet_requirements.png)     |    Your PC does not meet the requirements for the specified item.     |

## Windows Mixed Reality PC Compatibility Guidelines

The table below provides compatibliity guidelines for both Windows Mixed Reality Ultra PCs and Windows Mixed Reality PCs.<br><br>

<table>
<tr>
<th style="width:20%"></th><th style="vertical-align: middle; text-align: center; width:40%">Windows Mixed Reality Ultra PCs</th><th style="vertical-align: middle; text-align: center; width:40%">Windows Mixed Reality PCs</th>
</tr><tr>
<td style="vertical-align: middle">Operating System</td><td colspan="2" style="vertical-align: middle; text-align: center;">Windows 10 Fall Creators Update (RS3) or later - Home, Pro, Business, Education.<br/>    (<b>Note</b>: Not supported on N versions or Windows 10 Pro in S Mode)</td>
</tr><tr>
<td style="vertical-align: middle">Processor</td><td style="vertical-align: middle; text-align: center;">Intel Core i5 4590 (4th generation), quad-core (or better) <br>AMD Ryzen 5 1400 3.4Ghz (desktop), quad-core (or better)</td><td style="vertical-align: middle; text-align: center;">Intel Core i5 7200U (7th generation mobile), dual-core with Intel&#174; Hyper-Threading Technology enabled (or better)</td>
</tr><tr>
<td style="vertical-align: middle">RAM</td><td style="vertical-align: middle; text-align: center;">8GB DDR3 (or better)</td><td style="vertical-align: middle; text-align: center;">8GB DDR3 dual channel (or better)</td>
</tr><tr>
<td style="vertical-align: middle">Free disk space</td><td colspan="2" style="vertical-align: middle; text-align: center;">At least 10 GB</td>
</tr><tr>
<td style="vertical-align: middle">Graphics Card</td><td style="vertical-align: middle; text-align: center;"><li>NVIDIA GTX 1060 (or greater) DX12-capable discrete GPU</li> <br><li>AMD RX 470/570 (or greater) DX12-capable discrete GPU </li><br><b>Note:</b> GPU must be hosted in a PCIe 3.0 x4+ Link slot</td><td style="vertical-align: middle; text-align: center;"><li>Integrated Intel&#174; HD Graphics 620 (or greater) DX12-capable integrated GPU <a href="https://en.wikipedia.org/wiki/List_of_Intel_graphics_processing_units">(check if your model is greater)</a></li> <br><li>NVIDIA MX150 (or greater) discrete GPU</li><br><li>965M (or greater) DX12-capable discrete GPU</li><br><li>AMD Radeon RX 460/560</li></td>
</tr><tr>
<td style="vertical-align: middle">Graphics Driver</td><td style="vertical-align: middle; text-align: center;">Windows Display Driver Model (WDDM) 2.2</td><td style="vertical-align: middle; text-align: center;">Windows Display Driver Model (WDDM) 2.2</td>
</tr><tr>
<td style="vertical-align: middle"><a href="Recommended-adapters-for-Windows-Mixed-Reality-Capable-PCs.md">Graphics display port</a></td><td style="vertical-align: middle; text-align: center;">HDMI 2.0 or DisplayPort 1.2</td><td style="vertical-align: middle; text-align: center;">HDMI 1.4 or DisplayPort 1.2</td>
</tr><tr>
<td style="vertical-align: middle">Display</td><td colspan="2" style="vertical-align: middle; text-align: center;">Connected external or integrated VGA (800x600) display (or better)</td>
</tr><tr>
<td style="vertical-align: middle"><a href="Recommended-adapters-for-Windows-Mixed-Reality-Capable-PCs.md">USB connectivity</a></td><td colspan="2" style="vertical-align: middle; text-align: center;">USB 3.0 Type-A or Type-C</td>
</tr><tr>
<td style="vertical-align: middle">Bluetooth connectivity (for <a href="Motion-controllers.md">motion controllers</a>)</td><td colspan="2" style="vertical-align: middle; text-align: center;">Bluetooth 4.0</td>
</tr><tr>
<td style="vertical-align: middle">Expected headset framerate</td><td style="vertical-align: middle; text-align: center;">90 Hz</td><td style="vertical-align: middle; text-align: center;">60 Hz</td>
</tr>
</table>

## Tools and Applications

### Windows 10

Install the most recent version of Windows 10 so your PC's operating system matches the platform for which you're building mixed reality applications.

You can install the most recent version of Windows 10 via **Windows Update** in **Settings** or by [creating installation media](https://www.microsoft.com/en-us/software-download/windows10). The current release notes provides information about the newest mixed reality features available with each release of Windows 10.

After you've confirmed that your PC has the most recent version of Windows 10, you will need to enable **Developer Mode** on your PC. You can navigate to **Settings** > **Update & Security** > **For developers** to access the **Use developer features** settings.

[insert picture]

If you are using an enterprise or corporate-managed PC (i.e. your PC is managed by an organization's IT department), you may need to contact them in order to update. 

Please note that Windows Mixed Reality Immersive (VR) headsets are not supported on **N** versions of Windows. 

### Visual Studio

Visual Studio is a fully-featured integrated development environment (IDE) for Windows and more. You'll use Visual Studio to write code, debug, test, and deploy your mixed reality applications.

**HoloLens (1st gen)**

Download and install [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/) for developing mixed reality applications for a HoloLens 1 device. Before you install Visual Studio, ensure that your pc meets the [system requirements](https://docs.unity3d.com/Manual/system-requirements.html) for Visual Studio.

During installation, you will be prompted to select workloads to install. Select the following workloads:

- Desktop development with C++
- Universal Windows Platform (UWP) development

**HoloLens 2**

Download and install [Visual Studio 2019 (16.2 or higher)](https://visualstudio.microsoft.com/downloads/) for developing mixed reality applications for a HoloLens 2 device. Before you install Visual Studio, ensure that your pc meets the [system requirements](https://docs.unity3d.com/Manual/system-requirements.html) for Visual Studio.

Please note that there are some known issues with debugging mixed reality apps in Visual Studio 2019 version 16.0. Please ensure that you update Visual Studio 2019 to version 16.2 or higher.

During installation, you will be prompted to select workloads to install. Select the following workloads:

- Desktop development with C++
- Universal Windows Platform (UWP) development

### Windows 10 SDK

The Windows 10 SDK provides the latest headers, libraries, metadata, and tools for building Windows 10 apps.

**HoloLens (1st gen)**

If you are developing applications for desktop Windows Mixed Reality headsets or HoloLens (1st gen), you can use the Windows SDK installed by Visual Studio 2017.

**HoloLens 2**

To build HoloLens 2 apps, you must install the [Windows SDK](https://developer.microsoft.com//windows/downloads/windows-10-sdk), build 18362 or later.

### Emulator

The HoloLens Emulator lets you test holographic applications on your PC without a physical HoloLens. It also includes the HoloLens development toolset. The human and environmental inputs that are usually read by HoloLens sensors are simulated from your keyboard, mouse, or Xbox controller. Applications don't need to be modified to run on the emulator as applications do not know that they aren't running on a real HoloLens. To learn more about getting started with the emulator, see [Using the HoloLens Emulator](https://docs.microsoft.com/en-us/windows/mixed-reality/using-the-hololens-emulator).

**HoloLens (1st gen)**

The HoloLens Emulator uses Hyper-V with RemoteFx for hardware accelerated graphics. Please note that Windows 10 Home Edition does not support Hyper-V or the HoloLens Emulator.

Ensure that **Hyper-V** has been enabled on your system by navigating to **Control Panel** > **Programs** > **Programs and Features** > **Turn Windows Features on or off**. Ensure that **Hyper-V** is selected for the Emulator installation to be successful.

Download and install the latest version of the [Emulator](https://go.microsoft.com/fwlink/?linkid=2065980) for HoloLens (1st gen).

**HoloLens2**

The HoloLens Emulator uses GPU-PV for hardware accelerated graphics. The HoloLens 2 Emulator requires the Windows 10 October 2018 update or later.

Download and install the latest version of the [Emulator](https://go.microsoft.com/fwlink/?linkid=2118321) for HoloLens 2.

## Immersive (VR) Headset Development PC System Requirements

The guidelines provided below are the current minimum and recommended specs for your immersive (VR) headset development PC. The guidelines below are not to be confused with the minimum PC hardware compatibility guidelines which outlines the consumer PC specs to which you should target your immersive headset application or game.

If your immersive headset development PC does not have full-sized HDMI and/or USB 3.0 ports, you will need [adapters](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/recommended-adapters-for-windows-mixed-reality-capable-pcs) to connect your headset.

There are currently [known issues](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/troubleshooting-windows-mixed-reality) with some hardware configurations, particularly notebooks that have hybrid graphics.<br><br>

<table>
<tr>
<th></th><th> Minimum</th><th> Recommended</th>
</tr><tr>
<td> Processor</td><td> <b>Notebook:</b> Intel Mobile Core i5 7th generation CPU, Dual-Core with Hyper Threading <b>Desktop:</b> Intel Desktop i5 6th generation CPU, Dual-Core with Hyper Threading <b>OR</b> AMD FX4350 4.2Ghz Quad-Core equivalent</td><td> <b>Desktop:</b> Intel Desktop i7 6th generation (6 Core) <b>OR</b> AMD Ryzen 5 1600 (6 Core, 12 threads)</td>
</tr><tr>
<td> GPU</td><td> <b>Notebook:</b> NVIDIA GTX 965M, AMD RX 460M (2GB) equivalent or greater DX12 capable GPU <b>Desktop:</b> NVIDIA GTX 960/1050, AMD Radeon RX 460 (2GB) equivalent or greater DX12 capable GPU</td><td><b>Desktop:</b> NVIDIA GTX 980/1060, AMD Radeon RX 480 (2GB) equivalent or greater DX12 capable GPU</td>
</tr><tr>
<td> GPU driver WDDM version</td><td colspan="2"> WDDM 2.2 driver</td>
</tr><tr>
<td> Thermal Design Power</td><td colspan="2"> 15W or greater</td>
</tr><tr>
<td> Graphics display ports</td><td colspan="2"> 1x available graphics display port for&#160;headset (HDMI 1.4 or DisplayPort 1.2 for 60Hz headsets, HDMI 2.0 or DisplayPort 1.2 for 90Hz headsets)</td>
</tr><tr>
<td> Display resolution</td><td colspan="2"> Resolution: SVGA (800x600) or greater Bit depth: 32 bits of color per pixel</td>
</tr><tr>
<td> Memory</td><td> 8&#160;GB of RAM or greater</td><td> 16 GB of RAM or greater</td>
</tr><tr>
<td> Storage</td><td colspan="2"> &gt;10 GB additional free space</td>
</tr><tr>
<td> USB Ports</td><td colspan="2"> 1x available USB port for headset (USB 3.0 Type-A) <b>Note: USB must supply a minimum of 900mA</b></td>
</tr><tr>
<td> Bluetooth</td><td colspan="2"> Bluetooth 4.0 (for accessory connectivity)</td>
</tr>
</table>