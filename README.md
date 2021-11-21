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
