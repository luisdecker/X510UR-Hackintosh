# X510UR-Hackintosh
Files and info my build of a Hackintosh on a ASUS X510UR-BQ292T

This is a work in progress guide, that shows only what worked for me. I'm not any kind of hackintosh expert nor have access to a myriad of hardwares, so, I will only answer questions about this specific hardware and some related ones (VivoBook X510* mostly)

## Bootloader

Actually I'm using OpenCore 0.6.6 as bootloader. The actual installation of the OS is a **Big Sur** update from a previous Mojave that I did with clover, so if you are doing a fresh install, follow the [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## Status of the system

### :heavy_check_mark: Networking
I'm using [itlwm](https://openintelwireless.github.io/itlwm/) to enable the Intel Wifi card (Intel(R) Dual Band Wireless AC 8275). 

#### Relevant Kexts
- AirportItlwm.kext

### :heavy_check_mark: Graphics
Only intel integrated HD620 shared memory graphics are avaible. The 930MX is explicitly deactivated. Following some [directions](https://www.reddit.com/r/hackintosh/comments/gjksrk/smbios_framebuffer_and_performance/), I configured it as as UHD617 due to performance issues.

#### Relevant Kexts:
- WhateverGreen.kext

### :heavy_check_mark: Pointing device and keyboard
You may need a usb mouse to install the hack, as touchpad may wont work until later on. 

#### Relevant Kexts:
- VoodooI2C.kext
- VoodooI2CHID.kext
- VoodooPS2Controller.kext

### :heavy_check_mark: Bluetooth
Working normally with the devices I use.

#### Relevant Kexts
- IntelBluetoothInjector.kext
- IntelBluetoothFirmware.kext

### :heavy_check_mark: Battery Measurement
Working normally, but reporting *Service Needed*, but wont affect anything.

#### Relevant Kexts
- SMCBatteryManager.kext

#### Relevant DSDT's
- SSDT-BATT.aml

### :heavy_check_mark: Sound 
:heavy_check_mark: Internal speakers 
 
:heavy_check_mark: Internal Microphone 

:heavy_check_mark: Bluetooth Speakers 

:heavy_check_mark: USB Microphone 

#### Relavant Kexts
- AppleALC.kext

### CPU power scheduling
I tuned CPUFriend (Using CPUFriendFriend) to a more performance-oriented frequecy scheduler. 

#### Relevant Kexts
- CPUFriend.kext

### ✔️ Sleep
Aparently working. Had to apply a DSDT patch so to avoid instant wake from LAL, following guide provided in [this guide](https://dortania.github.io/OpenCore-Post-Install/usb/misc/instant-wake.html). 

#### Relevant SDST's
- SSDT-GPRW.aml

# EFI
The EFI folder attached is the one I use to boot my Hack. The kexts attached are the ones recommended by OpenCore Install Guide, and the ones listed above. Fixes intel graphics, touchpad, battery indicator, audio, bluetooth and Wifi. 

# Guide

Follow the [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/). Some DSDT's, kexts and configurations here presented may be used before the install to fix some of the issues I mentioned above.
