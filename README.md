# X510UR-Hackintosh
Files and info my build of a Hackintosh on a ASUS X510UR-BQ292T

This is a work in progress guide, that shows only what worked for me. I'm not any kind of hackintosh expert nor have access to a myriad of hardwares, so, I will only answer questions about this specific hardware and some related ones (VivoBook X510* mostly)

#### Networking
The only tested networking sollution in my build was Android usb-tethering my wifi connection. You can test a external wifi card or ethernet card. 

#### Graphics
Only intel integrated HD620 shared memory graphics are avaible. The 930MX is explicitly deactivated. 

#### Pointing device
You may need a usb mouse to install the hack, as touchpad wont work until later on. 

## EFI
The EFI folder I use to boot my Hack. Have fixes that I found in a lot of places, thanks to the original authors of every kext, DSDT patch and config.plist present.

Fixes intel graphics, touchpad, battery indicator, audio, and android USB tethering (as X510UR dons't have a ethernet port and the default intel wifi card is not compatible)

# Guide
(Scratch)

### 1) Prepare bootable usb stick and Install 
I followed the process described [here](https://github.com/nguyentrucxinh/ASUS-VivoBook-X510UQR-Hackintosh/blob/master/Guide.md). Check your BIOS configuration and follow the guide. Stop before "Post Installation"

You may move the EFI folder to the EFI folder of the installation media so it can boot.

### 2) Copy EFI folder to you EFI/ESP folder 
This will enable you to boot from the installed MacOS. Check your boot options to boot from clover. 

### 3) ????

### 4) Profit! 
