# Optiplex-9020-USFF-Hackintosh
This is my Hackintosh build using a Dell Optiplex 9020 Ultra Small Form Factor (in the Hackintosh community, also known as a OptiMac) using OpenCore.

 ![alt test](/Pictures/2022-07-07_10-57-26.png)
 ![alt test](/Pictures/OptiMac2.jpg)

# PC specifications:
- OS's installed: Monterey dualbooted with Windows 11 Pro
- PC Model: Dell Optiplex 9020 USFF (Ultra Small Form Factor)
- Processor: Intel i5-4590s @ 3.00 Ghz (Haswell)
- RAM: 16GB DDR3
- Storage: 128 GB SSD x2: MacOS and Windows
- Graphics card: Intel HD Graphics 4600
- Using a Display port to HDMI adapter to connect to my TV
  
# Notes:
- I'm not responsible for any harm done to your PC :-) Use my experiences and EFI at your own risk, even though I think this doesn't do much harm ;-).
- Most of the things I did went according @ trs96 his outstanding guides on: 
https://www.tonymacx86.com/threads/the-dell-optimac-big-sur-opencore-thread.302383/
- AMD GPU is NOT supported/tested and will fail to work without changes to the EFI.

# Create your USB stick with your pre-made EFI:
Please see this page:
https://github.com/joostiphone/MacOS-USB-Installer

 ![alt test](/Pictures/USB-STICK-VENT-MONT.png)

# BIOS Settings (from tonymacx86.com):
https://www.tonymacx86.com/threads/the-dell-optimac-big-sur-opencore-thread.302383/

# OpenCore
OpenCore is working very well. A small how-to here: 

PRECAUSION:
- I'm using OpenCore. You can download the latest build from here which you can use during the EFI creation as per below (or use mine...): https://github.com/acidanthera/OpenCorePkg/releases
- Also great info from: https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory

- USB preparation and installation of Big Sur/Monterey according this video:
https://www.youtube.com/watch?v=J22vqnS-QZ4&t=2s
- Create your EFI:
https://www.youtube.com/watch?v=XyDJMNMFi6I&t=58s
- When the EFI is done, add your SSDT's and DTSD's to the EFI partition using OpenCoreConfigurator to mount the EFI
- After that, create your own Serial Number using OpenCoreConfigurator

# Serial number:
You need to make your own serial number, so that your iCloud etc. will work without using someone else his serial number. In OC GEN-X or in OpenCore Configurator you can generate a new one if you don't have one yet, or if you need a new one.

# Updating Hackintosh (MacOS)
- In general; watch others do first to see if they succeed 
- Make sure first to install the latest Kext files
- Install latest OpenCore; but first make sure that this works according other users. Latest OpenCore build:
https://github.com/acidanthera/OpenCorePkg/releases

# Kexts:
Make sure (!) you are using the latest kexts: 

- AppleALC.kext
https://github.com/acidanthera/applealc/releases
- IntelMausi.kext
https://github.com/acidanthera/IntelMausi/releases
- SMCProcessor.kext
It's part of the VirtualSMC zip as per below kext
- USBInjectAll.kext
https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/
- Lilu.kext
https://github.com/acidanthera/Lilu/releases
- WhateverGreen.kext
https://github.com/acidanthera/WhateverGreen/releases
- VirtualSMC.kext
https://github.com/acidanthera/VirtualSMC/releases

For convenvience purposes, use either OpenCore Configurator or Hackintool to mount EFI and update the Kexts. I always provide the latest Kexts in my EFI as per below.

# Update your OpenCore EFI (small how-to)
![alt test](Pictures/OpenCoreUpdate.png)

 # Option 1 (easy): Update using HackinDROM 
 Download the app here:
 https://hackindrom.zapto.org 
 
 and watch a how-to here:
 https://www.youtube.com/watch?v=xRuerrG-lAU&t=50s
 
 # Option 2 (time consuming): Manually
https://github.com/joostiphone/Update-OpenCore-to-latest-version

# Latest Changes on uploaded EFI (without a Serial Number):
Please note that I only use the latest Stable released versions of MacOS and OpenCore (so no beta's, nighly builds or latest commitments).

(Item 0 is the oldest):

0. Installed my system succesfully using OpenCore 0.6.0
1. Tweaked it.
2. Updated to every latest Big Sur beta and OpenCore beta version.
3. 13-Oct-2020: Updated to latest Public Beta (20A5384c) and latest final OpenCore Build (v0.6.2).
4. 23-Nov-2020: Updated to latest Big Sur version 11.0.1 (20B29) and latest OpenCore build (v0.6.3).
5. 20-Jan-2021: Updated to latest Big Sur version 11.1 (20C69) and latest OpenCore build (v0.6.6).
6. 13-Feb-2021: Updated to latest Big Sur version 11.2.1 (20D74).
7. 25-March-2021: Updated to latest Big Sur version 11.2.3 (20D91) and latest OpenCore build (v0.6.7).
8. 17-April-2021: Updated to latest OpenCore build (0.6.8). 
9. 28-April-2021: Updated to MacOS 11.3 (20E232), using OpenCore v0.6.8.
10. 9-May-2021: Updated to MacOS 11.3.1 (20E241), using OpenCore v0.6.8 (OC 0.6.9 EFI will follow soon).
11. 9-May-2021: Updated to latest OpenCore build (0.6.9).
12. 12-June-2021: Updated to MacOS 11.4 (20F71), and Updated to latest OpenCore build (0.7.0).
13. 11-July-2021: Updated to latest OpenCore build (0.7.1), and preparing for MacOS Monterey. Still using Big Sur though!
14. 11-October-2021: IMPORTANT, due to Monterey not supporting older Mac's, we needed to update the SMBIOS version to Macmini7,1. This means that you NEED to create a new serial etc. for your system. Do this according to: https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#fixing-imessage-and-other-services-with-opencore I'm now using latest OpenCore build (0.7.4), and Monterey. Updated to MacOS 12.0 Beta 9.
15. 11-November-2021: Updated to latest OpenCore build (0.7.5), and updated to MacOS 12.0.1 (21A559).
16. 27-2-2022: OptiMac Monterey 12.2.1 (21D62) OpenCore 0.7.8.
17. 22-3-2022: OptiMac Monterey 12.3 (21E230) OpenCore 0.7.9.
18. 7-7-2022: OptiMac Monterey 12.4 OpenCore 0.8.2.
19. 27-10-2022: Tried Ventura, but too much problems for now. Will try again later. 
20. 30-10-2022: Going back to OptiMac Monterey 12.6.1 OpenCore 0.8.3. / 0.8.5
21. 3-11-2022: got Ventura to work including the HD4600 using OCLP 0.5.1. resulting into 1536MB of memory. For now I will wait for some development of OCLP or HD4000 Patch by Chris1111 to be updated for Ventura. For now, I recommend to stay on Monterey. 

# Download my latest EFI here (zip file):
![alt test](Pictures/Apple-icon.png)

Download here. The EFI is without my serial number, so you need to enter your own using OpenCore Configurator:

# Big Sur (OpenCore)
https://mega.nz/folder/R0xwBAKJ#4hIlvkFZhdFMzu5AvSbppQ

# Monterey (OpenCore)
https://mega.nz/folder/t04m2AoJ#AmwIXnWD5GFv-X5kxCWFBQ

![alt test](Pictures/platforminfo.png)

# Confirmed working:
- CPU, RAM, Fans, Cooling etc. ✔ Stable temps.
- Ethernet ✔
- Graphics ✔
- HDMI (via adapter, make sure that you use the DisplayPort output nearest to the VGA port) ✔
- Sleep/wake Function ✔
- Power Management ✔
- App Store ✔
- iMessage ✔
- iCloud ✔
- FaceTime ✔
- USB with 2.0, 3.0 Ports ✔
- Bootloader ✔
- Encryption (FileVault2) ✔ 
- HDMI Audio ✔
- Volume Hotkeys ✔
- No WiFi and Bluetooth (there is no WiFi/BT module on this board, and I'm not using a Fenvi card here due to the USFF design)
- AirDrop - No, due to lack if WiFi/BT module
- HandOff - No, due to lack if WiFi/BT module
- Side Car - No, due to lack if WiFi/BT module

# Credits:
https://github.com/joostiphone/Credits/blob/main/README.md

# Resources
- https://www.tonymacx86.com/threads/the-4k-dell-optimac-big-sur-opencore-thread-dell-optiplex-7020-and-9020.302383/
- https://hackintosh.gitbook.io 
- https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory
- https://github.com/acidanthera/OpenCorePkg/releases
- https://github.com/williambj1/OpenCore-Factory/releases
- https://mackie100projects.altervista.org/download-opencore-configurator/
- https://github.com/Pavo-IM/OC-Gen-X
- https://github.com/Pavo-IM/ocbuilder
