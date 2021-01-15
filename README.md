<!-- markdownlint-disable MD024 MD033 -->
# Hackintosh for [Acer Swift SF314-52-371C][snlookup]

_An attempt to get macOS Catalina running on an old, low-end laptop nobody cares about._

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

[IntelMausi][intelmausi]: `1.0.5-DEBUG`.

### USB

[USBInjectAll][usbinjectall]: `2018-1108` (Debug).

### WiFi

[AirportItlwm][airportitlwm]: `1.2.0_stable_Catalina`.

### Bluetooth

[IntelBluetoothFirmware][intelbluetoothfirmware]: `1.1.2`

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
