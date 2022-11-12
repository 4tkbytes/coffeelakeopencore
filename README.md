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
- IDK WiFi and Bluetooth

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

###How I did it:

dreamwhite#0001 first started off with making the EFI, then I grabbed an offline installer from Olarila. Now you might stop and think that Olarila is bad, but you can also use it as an offline installer. I paired up my efi with Olarila USB and installed it. I only did this because I did not have a stable internet connection. After macOS installed, I wiped my usb, added com.apple.recovery.boot and the EFI, and then I booted into macOS. It as successfully done. 


Credits: 
Thank you to dreamwhite#0001 on discord he helped me throughout the whole process. 
