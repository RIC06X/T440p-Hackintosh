
# T440p-Hackintosh

![this_mac 10.15.2](https://github.com/RIC06X/T440p-Hacintosh/blob/master/images/about_this_mac.png)

## OS Support

MacOS Catalina 10.15.2

### Laptop Specs

- Model: T440p
- Screen Resolution: 1920*1080
- CPU: i7-4710MQ
- RAM: 16G DDDR3
- Hard Drive: M.2 SATA 128G, SATA SAMSUNG 860 Pro 256G, Optical Drive SATA Toshiba 1Tb
- WiFi card: BCM94352Z

### What's working?

- All USB Ports
- Headphone jack
- Speaker
- Microphone
- mini DP (MacOS does NOT support daisy chain, only support 1 monitor)
- WiFi (Replaced original Intel card with BCMBCM94352Z, needs to remove BIOS whitelist)
- Bluetooth
- Touchpad and Trackpoint
- Web Cam
- Power Management
- Brightness Control
- Graphic Acceleration 
- Battery Status
- Disabled NVIDIA GPU
- Airdrop
- Handoff
- Facetime
- iMessage

### What's NOT working?

- VGA port
- SD Card Reader 
- Fingerprint Scanner

### What's my build different from others' build?

- Fixed six apple logo before login screen by change `HorizontalSyncPulseWidth` to `0x64` in config.plist
- Fixed MacOS Catalina BCM94352Z Bluetooth not working, Slow Boot, Slow Shutdown issues by Replacing brcm* kext with BrcmBluetoothInjector, BrcmFirmwareData, and BrcmPatchRAM3.kext

### Catalina Kext Installation 

Follow guide of the Hackintool Method
<https://www.tonymacx86.com/threads/guide-installing-3rd-party-kexts-el-capitan-sierra-high-sierra-mojave-catalina.268964/>

## Installation Guide

Please follow guide in <https://www.tonymacx86.com/threads/guide-lenovo-thinkpad-t440p.233282/> but with few modification in order to get Catalina working

### During **Creating USB Installer** 
At the last step of *Add kexts to EFI/Clover/kexts/Other*:
 
- Please copy all kexts at <https://github.com/RIC06X/T440p-Hackintosh/tree/master/EFI/CLOVER/kexts/Other> to your USB installer's `EFI/Clover/kexts/Other`
- If you laptop specs is identical with mine, copy my plist at <https://github.com/RIC06X/T440p-Hackintosh/tree/master/EFI/CLOVER>

### During **Post installation**

the first step *Install kexts into HDD/SSD* should replaced by:

- download kexts at <https://github.com/RIC06X/T440p-Hackintosh/tree/master/kexts>
- use Hackintool I mentioned above to install kexts

Follow the rest procedures at tonymacx86 guide, and you are good to go

