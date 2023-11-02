# Lenovo V110-15ISK Hackintosh OpenCore macOS Ventura
EFI folder to run macOS Ventura version on Lenovo V110-15ISK Laptop using OpenCore as bootloader.
## [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)

## About this Laptop

![Screenshot 2023-10-28 at 12 11 06](https://github.com/ciccio-90/Lenovo_V110-15ISK_Hackintosh_OpenCore_macOS_Sonoma/assets/66642459/809ad572-88f2-4eb8-9992-861a0693aed4)

### Original Hardware

Type | Specification | Status
:---------|:---------|:----------
Motherboard	| Phoenix BIOS 1KCN51WW | Working
CPU | Intel(R) Core(TM) i3-6100U CPU @ 2.03GHz | Working
Ethernet | Realtek RTL8100 PCI Express Gigabit Ethernet Controller | Working
Wi-Fi | RTL8821E 802.11ac | Not Working (Incompatible with hackintosh)
Bluetooth | Working
GPU | Intel Skylake GT2 HD Graphics 520 | Working
Audio | Realtek ALC236 | Working
HDMI | Intel Skylake HDMI | Working
Keyboard & Touchpad | Synaptics | Working
Webcam | EasyCamera | Working
Card Reader | Realtek RTS5129 USB 2.0 Card Reader | Working
USB | Sunrise Point-LP USB 3.0 xHCI Controller | Working
### Modifications
Type | Status
:--------- |:---------
Samsung SSD 850 EVO 150GB Media SATA | Working
RAM 8.00 GB | Working
Disc Burning | Working
### Used Kexts 
 
Kext | Info 
:---------|:---------
[Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Arbitrary kext and process patching on macOS.
[IntelBTPatcher.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | A Lilu base patcher that fix Intel Bluetooth.
[IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | Intel Bluetooth Drivers for macOS.
[BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM/releases) | Needed for all non-native Bluetooth devices.
[AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | Native macOS HD audio for not officially supported codecs.
[RealtekRTL8100.kext](https://github.com/Mieze/RealtekRTL8100) | OS X open source driver for the Realtek RTL8111/8168 family.
[VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC emulator layer.
[SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for measuring battery readouts on laptops.
[SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring CPU temperature.
[SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring fan speed.
[VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases) | For systems with PS2 keyboards, mice, and trackpads.
[WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs.
[RealtekCardReader.kext](https://github.com/0xFireWolf/RealtekCardReader/releases) | An unofficial Realtek PCIe/USB-based SD card reader driver for macOS.
[RealtekCardReaderFriend.kext](https://github.com/0xFireWolf/RealtekCardReaderFriend/releases) | A Lilu plugin that makes System Information recognize your Realtek card reader as a native one.
### Used SSDTs
SSDT | Info
:---------|:---------
[SSDT-PLUG-DRTNIA.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml) | Used for enabling Apple's XCPM in macOS, allowing for far better CPU power management.
[SSDT-EC-USBX-LAPTOP.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-LAPTOP.aml) | Used for disabling your real Embedded controller and creating a fake one for macOS to play with. USBX portion is used for injection USB power properties missing on Skylake and newer.
[SSDT-PNLF.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml) | Used for controlling the backlight on internal displays such as AIOs and laptops.