# PANZERS_RYZEN

https://item.jd.com/10034287970345.html

## Specification

- Motherboard: ASRock X300TM-ITX (https://www.asrock.com/mb/AMD/X300TM-ITX/index.asp)
    - BIOS: Version 1.20 (https://download.asrock.com/BIOS/AM4/X300TM-ITX(1.20)ROM.zip)
    - Manual: User Manual (https://download.asrock.com/Manual/X300TM-ITX.pdf)


- WiFi: Comfast CF-812AC (https://comfastlink.com/comfast-cf-812ac-1300mbps-usb-3-wifi-network-card)
    - Driver Program: Mac (http://en.comfast.com.cn/index.php?m=content&c=index&a=show&catid=30&id=348)


- Bluetooth: CSR8510 A10 (https://item.jd.com/11078472771.html)
    - BlueToolFixup.kext + Brcm{FirmwareData,PatchRAM3}.kext

## Pre-Install

https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html#amd-bios-settings

### BIOS

- `Boot` - `Fast Boot` = Disabled
- `Security` - `Secure Boot` - `Secure Boot` = Disabled
- `Advanced` - `Onboard Devices Configuration` - `Serial Port` = Disabled
- `Boot` - `CSM(Compatibility Support Module)` - `CSM` = Disabled
- `Advanced` - `CPU Configuration` - `IOMMU` = Disabled


- `Advanced` - `Storage Configuration` - `SATA Mode` = AHCI

## Post-Install

https://github.com/DavidS95/Smokeless_UMAF

### BIOS

- Device Manager
    - PCI Subsystem Settings
        - Above 4G Decoding = [x]
        - Re-Size BAR Support = \<Auto>
    - Setup - Advanced - USB Configuration - XHCI Hand-off = \<Enabled>

### Credit

https://www.reddit.com/r/hackintosh/comments/15pzwhw/nootedred_and_vendor_locked_uma_buffer_sizes/

- Device Manager - AMD CBS - NBIO Common Options - GFX Configuration
    - iGPU Configuration = <UMA_SPECIFIED>
    - UMA Frame fuffer Size = <2G>

## Accessories

- https://item.jd.com/100027284859.html
- https://item.taobao.com/item.htm?id=680228842890
