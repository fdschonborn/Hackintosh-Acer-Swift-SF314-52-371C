<!-- markdownlint-disable MD024 MD033 -->

<div align="center">

# Hackintosh for [Acer Swift SF314-52-371C][snlookup]

_An attempt to get macOS Catalina running on an old, low-end laptop nobody cares about._

</div>

## [OpenCore][opencore]

Version: `0.6.5-DEBUG`.

## [Firmware Drivers][firmware-drivers]

### Required

- `OpenRuntime.efi`: From OpenCorePkg.
- [`HfsPlus.efi`][hfsplus]: Commit `192ed42`.

## [Kexts][kexts]

### Required

- [VirtualSMC][virtualsmc]: `1.1.9-DEBUG`.
- [Lilu][lilu]: `1.5.0-DEBUG`.
  - Removed ([Reference][lilu-removed-reference]):
    - `SMCBatteryManager.kext` (temporary)
    - `SMCDellSensors.kext`
    - `SMCLightSensor.kext`

### Graphics

[WhateverGreen][whatevergreen]: `1.4.6-DEBUG`.

### Audio

[AppleALC][applealc]: `1.5.6-DEBUG`.

### Ethernet

[IntelMausi + IntelSnowMausi][intelmausi]: `1.0.5-DEBUG`.

### USB

[USBInjectAll][usbinjectall]: `2018-1108` (Debug).

### WiFi

[AirportItlwm][airportitlwm]: `1.2.0_stable_Catalina`.

### Bluetooth

[IntelBluetoothFirmware][intelbluetoothfirmware]: `1.1.2`.

### Input

[VoodooInput][voodooinput]: `1.0.9-DEBUG`.
[VoodooI2C][voodooi2c]: `2.6.3`.
[VoodooPS2][voodoops2]: `2.2.0-DEBUG`.
[VoodooRMI][voodoormi]: `1.3-Debug`.

## [SSDTs][ssdts]

### CPU

[SSDT-PLUG][ssdt-plug]: Prebuilt (commit `3756ef9`).

### EC

[SSDT-EC-USBX][ssdt-ec-usbx]: Prebuilt (`SSDT-EC-USBX-LAPTOP.aml`, commit `3756ef9`).

### Backlight

[SSDT-PNLF][ssdt-pnlf]: Prebuilt (`SSDT-PNLF.aml`, commit `3756ef9`).

### Trackpad

[SSDT-GPI0/XOSI][ssdt-gpi0-xosi]: Prebuilt (commit `3756ef9`).

## Resources

- [OpenCore Sanity Checker][opencore-sanity-checker].

<div align="center">

<br/>

**_TODO_**

</div>

<!-- Links -->

[snlookup]: https://snlookup.com/acer-swift-sf314-52-ultra-thin-nx-gplal-003-p110150
[opencore]: https://github.com/acidanthera/OpenCorePkg
[firmware-drivers]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers
[hfsplus]: https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi
[kexts]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#kexts
[virtualsmc]: https://github.com/acidanthera/VirtualSMC
[lilu]: https://github.com/acidanthera/Lilu
[lilu-removed-reference]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#virtualsmc-plugins
[whatevergreen]: https://github.com/acidanthera/WhateverGreen
[applealc]: https://github.com/acidanthera/AppleALC
[intelmausi]: https://github.com/acidanthera/IntelMausi
[usbinjectall]: https://bitbucket.org/RehabMan/os-x-usb-inject-all
[airportitlwm]: https://github.com/OpenIntelWireless/itlwm
[intelbluetoothfirmware]: https://github.com/OpenIntelWireless/IntelBluetoothFirmware
[voodooinput]: https://github.com/acidanthera/VoodooInput
[voodooi2c]: https://github.com/VoodooI2C/VoodooI2C
[voodoops2]: https://github.com/acidanthera/VoodooPS2
[voodoormi]: https://github.com/VoodooSMBus/VoodooRMI
[ssdts]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#ssdts
[ssdt-plug]: https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html
[ssdt-ec-usbx]: https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html
[ssdt-pnlf]: https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html
[ssdt-gpi0-xosi]: https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad.html
[opencore-sanity-checker]: https://opencore.slowgeek.com/
