# How to set-up HoloLens 2 Emulator

You can download the latest [HoloLens Emulator update](https://docs.microsoft.com/windows/mixed-reality/using-the-hololens-emulator?WT.mc_id=github-mixedrealitycurriculum-ayyonet#installing-the-hololens-emulator) here:[ bit.ly/emulator2](http://bit.ly/emulator2). 

### Can the HoloLens Emulator run on my device?

Before installing the emulator, make sure your PC meets the following **hardware requirements**:

* [ ] 64-bit Windows 10 Pro, Enterprise, or Education
* [ ] 64-bit CPU
* [ ] CPU with 4 cores \(or multiple CPUs with a total of 4 cores\)
* [ ] 8 GB of RAM or more
* [ ] In the BIOS, the following features must be [supported and enabled](https://blogs.technet.com/b/iftekhar/archive/2010/08/09/enable-hardware-settings-in-bios-to-run-hyper-v.aspx):
  * Hardware-assisted virtualization
  * Second Level Address Translation \(SLAT\)
  * Hardware-based Data Execution Prevention \(DEP\)
* [ ] GPU requirements
  * DirectX 11.0 or later
  * WDDM 1.2 graphics driver or later \(1st gen\)
  * WDDM 2.5 graphics driver \(HoloLens 2 Emulator\)
  * The emulator might work with an unsupported GPU, but will be significantly slower
* [ ] You need to enable "**Hyper-V"** feature on your device before you can use the Emulator. 

{% hint style="warning" %}
**Windows 10 Home Edition** does **not support Hyper-V** or the HoloLens Emulator. The HoloLens 2 Emulator requires the **Windows 10 October 2018** update or later.
{% endhint %}

### How to check or enable "Hyper-V" settings?

{% embed url="https://youtu.be/y7IfnUXVzk8" caption="How to check or enable \"Hyper-V\" on your PC" %}

### How to install or update the Emulator?

{% embed url="https://youtu.be/mK-bCFWBmyE" caption="How to install or update HoloLens Emulator?" %}



