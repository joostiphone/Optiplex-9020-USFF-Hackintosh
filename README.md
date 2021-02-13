# Optiplex-9020-USFF-Hackintosh
This is my Hackintosh build using a Dell Optiplex 9020 Ultra Small Form Factor (in the Hackintosh community, also known as a OptiMac).

 ![alt test](/Pictures/OptiMac.jpg)

# PC specifications:
- OS's installed: Big Sur dualbooted with Windows 10 Pro
- PC Model: Dell Optiplex 9020 USFF (Ultra Small Form Factor)
- Processor: Intel i5-4590s @ 3.00 Ghz (Haswell)
- RAM: 16GB DDR3
- Storage: 128 GB SSD x2: MacOS and Windows 10
- Graphics card: Intel HD Graphics 4600
- Using a Display port to HDMI adapter to connect to my TV
  
 ![alt test](/Pictures/AboutOptiplex3.png)
  
# Confirmed working
- CPU, RAM, Fans, Cooling etc. ✔ Stable temps.
- Ethernet ✔
- Graphics ✔
- HDMI (via adapter) ✔
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

# Notes:
- I'm not responsible for any harm done to your PC :-) Use my experiences and EFI at your own risk, even though I think this doesn't do much harm ;-).

# Kexts:
Make sure (!) you are using the latest kexts: 

- FakeSMC.kext
https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads/
- USBInjectAll.kext
https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/
- Lilu.kext
https://github.com/acidanthera/Lilu/releases
- WhateverGreen.kext
https://github.com/acidanthera/WhateverGreen/releases

For convenvience purposes, use either OpenCore Configurator or Hackintool to mount EFI and update the Kexts.

# BIOS Settings (from tonymacx86.com):
https://www.tonymacx86.com/threads/the-4k-dell-optimac-big-sur-opencore-thread-dell-optiplex-7020-and-9020.302383/

# Work Procedure:
https://www.tonymacx86.com/threads/the-4k-dell-optimac-big-sur-opencore-thread-dell-optiplex-7020-and-9020.302383/

So far Big Sur with OpenCore is working very well. A small how-to here: 

PRECAUSION/Notes:
- You can download the latest build from here which you can use during the EFI creation as per below: https://github.com/acidanthera/OpenCorePkg/releases
- Also great info from: https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory
- Formally, OpenCore is still in beta, but releases are overall noted as RELEASE instead of DEVELOPMENT version. I always recommend to choose the RELEASE version.

- USB preparation and installation of Big Sur according this video:
https://www.youtube.com/watch?v=J22vqnS-QZ4&t=2s
- Create your EFI:
https://www.youtube.com/watch?v=XyDJMNMFi6I&t=58s
- When the EFI is done, add your SSDT's and DTSD's to the EFI partition using OpenCoreConfigurator to mount the EFI
- After that, create your own Serial Number using OpenCoreConfigurator

# Serial number:
You need to make your own serial number, so that your iCloud etc. will work without using someone else his serial number. In OC GEN-X or in OpenCore Configurator you can generate a new one if you don't have one yet, or if you need a new one.

# Updating Hackintosh
- In general; watch others do first to see if they succeed 
- Make sure first to install the latest Kext files
- Install latest OpenCore; but first make sure that this works according other users. Latest OpenCore build:
https://github.com/acidanthera/OpenCorePkg/releases

# Update your OpenCore EFI (small how-to)
https://github.com/joostiphone/Update-OpenCore-to-latest-version

# Extras
n/a

# Resources
https://www.tonymacx86.com/threads/the-4k-dell-optimac-big-sur-opencore-thread-dell-optiplex-7020-and-9020.302383/
https://hackintosh.gitbook.io 
https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory
https://github.com/acidanthera/OpenCorePkg/releases
https://github.com/williambj1/OpenCore-Factory/releases
https://mackie100projects.altervista.org/download-opencore-configurator/
https://github.com/Pavo-IM/OC-Gen-X
https://github.com/Pavo-IM/ocbuilder

# Latest Changes in uploaded Big Sur EFI (without a Serial Number):
(Item 0 is the oldest):

0. Installed my system succesfully using OpenCore 0.6.0
1. Tweaked it.
2. Updated to every latest Big Sur beta and OpenCore beta version.
3. 13-Oct-2020: Updated to latest Public Beta (20A5384c) and latest final OpenCore Build (v0.6.2).
4. 23-Nov-2020: Updated to latest Big Sur version 11.0.1 (20B29) and latest OpenCore build (v0.6.3).
5. 20-Jan-2021: Updated to latest Big Sur version 11.1 (20C69) and latest OpenCore build (v0.6.6).
6. 13-Feb-2021: Updated to latest Big Sur version 11.2.1 (20D74).

# Download my latest Big Sur EFI here:
https://mega.nz/folder/R0xwBAKJ#4hIlvkFZhdFMzu5AvSbppQ


