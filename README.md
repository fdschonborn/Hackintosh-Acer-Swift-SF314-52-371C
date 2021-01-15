<!-- markdownlint-disable MD033 -->
<div align="center">

# Hackintosh for [Acer Swift SF314-52-371C][snlookup]

_An attempt to get macOS running on an old, low-end laptop nobody cares about._

</div>

## [OpenCore][opencore]

Version: `0.6.5-DEBUG`.

## [Firmware Drivers][firmware-drivers]

- [`HfsPlus.efi`][hfsplus]: Commit `192ed42`.

## [Kexts][kexts]

- [VirtualSMC][virtualsmc]: `1.1.9-DEBUG`.
- [Lilu][lilu]: `1.5.0-DEBUG`.
  - Removed ([Reference][lilu-removed-reference]):
    - `SMCBatteryManager.kext` (temporary)
    - `SMCDellSensors.kext`
    - `SMCLightSensor.kext`
- [WhateverGreen][whatevergreen]: `1.4.6-DEBUG`.
- [AppleALC][applealc]: `1.5.6-DEBUG`.
- **TODO**

[snlookup]: https://snlookup.com/acer-swift-sf314-52-ultra-thin-nx-gplal-003-p110150
[opencore]: https://github.com/acidanthera/OpenCorePkg
[firmware-drivers]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers
[hfsplus]: https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi
[kexts]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html
[virtualsmc]: https://github.com/acidanthera/VirtualSMC
[lilu]: https://github.com/acidanthera/Lilu
[lilu-removed-reference]: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#virtualsmc-plugins
[whatevergreen]: https://github.com/acidanthera/WhateverGreen
[applealc]: https://github.com/acidanthera/AppleALC
