# M-Audio-Firewire

Install M-Audio Kernel Extension (Driver)

OS X 10.10.x Yosemite

OS X 10.11.x El Capitan

-----

This allows the installation of unsigned kernel extensions.

IT OPENS UP SEVERAL SECURITY VULNERABILITIES!

Proceed if you are ok with that.

-----

Disable System Integrity Protection - Skip this step for OS X 10.10 Yosemite

1. Boot up in Recovery Mode (CMD-R while turning on the Mac)
2. Open Terminal
3. Enter the following command...
   - ```csrutil disable```
4. Reboot

-----

Enable Developer Mode for Kernel Extensions

1. Open Terminal
2. Enter the following…
   	- ```sudo nvram boot-args=kext-dev-mode=1```
3. Copy M-AudioFireWireBeBoB.kext to /System/Library/Extensions/
4. Enter the following commands...
   	- ```cd /System/Library/Extensions/```
   	- ```sudo chmod -R 755 M-AudioFireWireBeBoB.kext```
   	- ```sudo chown -R root:wheel M-AudioFireWireBeBoB.kext```
5. Reboot (or see optional next section first)

-----

Optionally Install Additional Packages

1. Run each package (except M-Audio FireWire Kernel Extension.pkg) from 
   the “Extracted installer Packages” folder.
2. Reboot

This portion is not required for the Firewire kext to work and show up
in your audio applications.

-----

You can resecure your computer but it will disable the M-Audio extension
as it is unsigned. Here’s how...

1. Open Terminal
2. Enter the following command
   	- ```sudo nvram -d boot-args```
3. Reboot in Recovery Mode (CMD-R while turning on the Mac)
4. Open Terminal
5. Enter the following command...
   	- ```csrutil enable```
6. Reboot

-----

More Info here…

http://www.curvve.com/blog/guides/2014/os-x-10-10-yosemite-sound-driver-hack-for-m-audio-ni-and-more/
https://forums.developer.apple.com/thread/3981
http://osxdaily.com/2012/01/12/how-to-manually-install-kernel-extensions-in-mac-os-x/
