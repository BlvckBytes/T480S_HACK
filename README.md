# T480S Hackintosh (OpenCore)

With this setup, you'll get the following:

* ✅ Trackpad, Buttons, Trackpoint
* ✅ Mapped FN-Keys
* ✅ Mapped USB ports
* ✅ Fully working audio
* ✅ Sleep and LID-detection
* ✅ Fast boot time
* ✅ WiFi and BlueTooth

## Warnings

This repo is geared towards Monterey. If you use lower versions, you'll have to substitute `BlueToolFixup.kext` for `BrcmBluetoothInjector.kext`. Also, don't forget to create your own SMBIOS and use something like your WiFi-MAC as your ROM inside `config.plist`. Just using the EFI as is will maybe get you in trouble if you don't accomplish this step properly. I'm using BroadCom WiFi/BT hardware, so if you're using intel, change out the kexts.

## BIOS Settings

At the time of writing this, I am running Lenovo's UEFI BIOS Versin `N22ET65W (1.42)`. You don't necessarily have to have the exact same version, tho. There are a few key settings you need to adjust to have a smooth experience:

* Config
  * USB
    * USB UEFI BIOS Support - Enabled
  * Keyboard/Mouse
    * TrackPoint - Enabled
    * Trackpad - Enabled
    * F1-F12 as Primary Function - Disabled
    * Fn Sticky Key - Disabled
    * F1-F12 as Primary Function - Disabled
  * Display
    * Total Graphics Memory - 512MB
  * Power
    * Lid Sensor - Enabled
  * Thunderbolt(TM) 3
    * Thunderbolt BIOS Assist Mode - Disabled
    * Security Level - No Security
* Security
  * Security Chip
    * Security Chip - Disabled
  * Virtualization
    * Intel (R) Virtualization Technoloty - Enabled
    * Intel (R) VT-d Feature - Disabled
  * I/O Port Access
    * Ethernet LAN - Enabled
    * Wireless LAN - Enabled
    * Wireless WAN - Enabled if you have the module, Disabled otherwise
    * Bluetooth - Enabled
    * Memory Card Slot - Enabled
    * Smart Card Slot - Disabled (to save power)
    * Integrated Camera - Enabled
    * Microphone - Enabled
    * Fingerprint Reader - Disabled (to save power)
    * Thunderbolt (TM) 3 - Enabled
  * Computrace
    * Current Setting - Disabled
  * Secure Boot Configuration
    * Secure Boot - Disabled
  * Intel (R) SGX
    * Intel (R) SGX Control - Disabled
  * Device Guard
    * Device Guard - Disabled

While installing, it helps tremendously to go to `Startup` > `Boot` > and set `USB HDD` as the first option. This way, OpenCore can take over automatically while you do something else.