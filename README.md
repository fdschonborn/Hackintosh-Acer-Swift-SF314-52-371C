<!-- markdownlint-disable MD024 MD041 -->

# Hackintosh for [Acer Swift SF314-52-371C][snlookup]

An attempt to get macOS Catalina running on my old low-end laptop.

## [OpenCore][opencore]

Version: `0.6.9-DEBUG`.

## [Firmware Drivers][firmware-drivers]

### Required

- `OpenRuntime.efi`
- [`HfsPlus.efi`][hfsplus]

## [Kexts][kexts]

### Required

- [VirtualSMC][virtualsmc]: `1.2.3-DEBUG`.
  - Removed ([Reference][virtualsmc-removed-reference]):
    - `SMCDellSensors.kext`
    - `SMCLightSensor.kext`
- [Lilu][lilu]: `1.5.3-DEBUG`.

### Graphics

[WhateverGreen][whatevergreen]: `1.4.9-DEBUG`.

### Audio

[AppleALC][applealc]: `1.6.0-DEBUG`.

### Ethernet

[IntelMausi][intelmausi]: `1.0.6-DEBUG`.

### USB

[USBInjectAll][usbinjectall]: `2018-1108` (Debug).

### WiFi

[AirportItlwm][airportitlwm]: `1.3.0_stable_Catalina`.

### Bluetooth

[IntelBluetoothFirmware][intelbluetoothfirmware]: `1.1.2`.

### Input

[VoodooI2C][voodooi2c]: `2.6.5`.

Satellites:

- VoodooI2CHID

### Misc

- [ECEnabler][ecenabler]: `1.0.1-DEBUG`
- [BrightnessKeys][bkeys]: `1.0.1-DEBUG`

## [SSDTs][ssdts]

### CPU

[SSDT-PLUG][ssdt-plug]: Prebuilt.

### EC

[SSDT-EC-USBX-LAPTOP][ssdt-ec-usbx-laptop]: Prebuilt.

### Backlight

[SSDT-PNLF][ssdt-pnlf]: Prebuilt.

### Trackpad

[SSDT-XOSI][ssdt-xosi]: Prebuilt.

## Resources

- [OpenCore Sanity Checker][opencore-sanity-checker].

<!-- Links -->

[snlookup]: https://snlookup.com/acer-swift-sf314-52-ultra-thin-nx-gplal-003-p110150
[opencore]: https://github.com/acidanthera/OpenCorePkg
[firmware-drivers]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers
[hfsplus]: https://github.com/acidanthera/OcBinaryData/blob/95b7d4ccb9fea6af48641fc1f5bd4b57f747b235/Drivers/HfsPlus.efi
[kexts]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#kexts
[virtualsmc]: https://github.com/acidanthera/VirtualSMC
[lilu]: https://github.com/acidanthera/Lilu
[virtualsmc-removed-reference]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#virtualsmc-plugins
[whatevergreen]: https://github.com/acidanthera/WhateverGreen
[applealc]: https://github.com/acidanthera/AppleALC
[intelmausi]: https://github.com/acidanthera/IntelMausi
[usbinjectall]: https://bitbucket.org/RehabMan/os-x-usb-inject-all
[airportitlwm]: https://github.com/OpenIntelWireless/itlwm
[intelbluetoothfirmware]: https://github.com/OpenIntelWireless/IntelBluetoothFirmware
[voodooinput]: https://github.com/acidanthera/VoodooInput
[voodooi2c]: https://github.com/VoodooI2C/VoodooI2C
[ecenabler]: https://github.com/1Revenger1/ECEnabler
[bkeys]: https://github.com/acidanthera/BrightnessKeys
[ssdts]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#ssdts
[ssdt-plug]: https://github.com/dortania/Getting-Started-With-ACPI/blob/b8e37ede5ec68165918cfd611e2afd3075f7fe27/extra-files/compiled/SSDT-PLUG-DRTNIA.aml
[ssdt-ec-usbx-laptop]: https://github.com/dortania/Getting-Started-With-ACPI/blob/b8e37ede5ec68165918cfd611e2afd3075f7fe27/extra-files/compiled/SSDT-EC-USBX-LAPTOP.aml
[ssdt-pnlf]: https://github.com/dortania/Getting-Started-With-ACPI/blob/b8e37ede5ec68165918cfd611e2afd3075f7fe27/extra-files/compiled/SSDT-PNLF.aml
[ssdt-xosi]: https://github.com/dortania/Getting-Started-With-ACPI/blob/b8e37ede5ec68165918cfd611e2afd3075f7fe27/extra-files/compiled/SSDT-XOSI.aml
[opencore-sanity-checker]: https://opencore.slowgeek.com/
