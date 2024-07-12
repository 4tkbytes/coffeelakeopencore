# Coffee Lake Opencore Repository
Specs:

| Hardware | Name |
|----------|------|
| CPU | Intel(R) Core(TM) i7-8700 CPU @ 3.20GHz |
| (d)GPU | NVIDIA GeForce GT 1030 |
| (i)gpu | Intel(R) UHD Graphics 630 |
| Chipset | Intel(R) 300 Series Chipset (B365) |
| Audio Codec | Realtek ALC892 |
| Network Controllers (WiFi) | TP-Link 802.11ac Network Adapter |
| Network Controllers (Ethernet) | Intel(R) Ethernet Connection I219-V |
| Disk Drive | Samsung SSD 860 QVO 1TB|
| Disk Drive | CT1000BX 500SSD1 |


Kexts: 
- Lilu
- VirtualSMC
    - SMCProcessor
- WhateverGreen
- AppleALC
- IntelMausi
- USBToolBox
- BlueToolFixUp
- AirportBRCMFixup

SSDT:
- SSDT-AWAC
- SSDT-EC-USBX
- SSDT-PLUG
- SSDT-PMC

config.plist:
- Booter/Quirks
    - EnableWriteUnprotector ; Disabled
    - RebuildAppleMemoryMap & SyncRuntimePermissions ; Enabled
- Kernel/Quirks
    - AppleXcpmCfgLock ; enabled

### How I did it:

~~dreamwhite#0001 first started off with making the EFI, then I grabbed an offline installer from Olarila. Now you might stop and think that Olarila is bad, but you can also use it as an offline installer. I paired up my efi with Olarila USB and installed it. I only did this because I did not have a stable internet connection. After macOS installed, I wiped my usb, added com.apple.recovery.boot and the EFI, and then I booted into macOS. It as successfully done.~~ 

EDIT: 
1. i dont use olarila anymore. i didnt have internet at my house at the time of the first commit so using an olarila as an offline installer was the most easiest way to install. afterwards, i changed it to my efi. even which, i found other ways to make offline installer by myself instead of relying on olarila. 
2. the github repo is owned by me (on discord it is @192.168.1.101/tmobile customer service). i keep it on github to make it easier to see the changes and what to fix it.
3. if it is already built using an existing efi, i would have not known that since i got someone to help me build it for me (which makes it technically not a prebuilt if they know all my specifications and everything plus i helped troubleshoot my owwn problems and just asked them for assistance).


### Credits: 

Thank you to dreamwhite#0001 on discord he helped me throughout the whole process. 
