### Huananzhi X99-F8
###BIOS 2020/05/25 (GHX99015)

+ When using server (ECC) memory, error correction function is active
+ Timing Command Rate (CR) can take any specified value from 1 to 3

This BIOS is compatible with [Ultimate Patcher Tool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods#Ultimate-Patcher-Tool) (latest version of the program is recommended)

A version with the beeper disabled is also available

*v011:*
* + added support for Resizable BAR (SAM) * updated the logo to the official one (taken from the new BIOS version) and enabled its display by default
* added +3.3V to HardwareMonitor
* BIOS base GHX99015
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu items "Memory Frequency" and "OverClocking Feature" will no longer disappear
* menu items "Memory Thermal", "CPU C State Control", "Program PP0_CURT_CFG_CTRL_MSR", "SOCKET RAPL Config", "Per-Socket Configuration" and "PCI Subsystem Settings" are open
* BCLK 100.00MHz (0.00% SSC)

*v010:*
* + menu item "Memory Thermal" is open
* - previously enabled ASPM support has been removed, because There was a compatibility issue with AMD Radeon RX 6000 series video cards
* updated the logo to the official one (taken from the new BIOS version) and enabled its display by default
* added +3.3V to HardwareMonitor
* BIOS base GHX99015
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu items "Memory Frequency" and "OverClocking Feature" will no longer disappear
* menu items "CPU C State Control", "Program PP0_CURT_CFG_CTRL_MSR", "SOCKET RAPL Config", "Per-Socket Configuration" and "PCI Subsystem Settings" are open
* BCLK 100.00MHz (0.00% SSC)

*v009:*
* - the PCI-E bus fix has been removed, because some video cards stopped starting altogether
* updated the logo to the official one (taken from the new BIOS version) and enabled its display by default
* added +3.3V to HardwareMonitor
* BIOS base GHX99015
* ASPM support included
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu items "Memory Frequency" and "OverClocking Feature" will no longer disappear
* menu items "CPU C State Control", "Program PP0_CURT_CFG_CTRL_MSR", "SOCKET RAPL Config", "Per-Socket Configuration" and "PCI Subsystem Settings" are open
* BCLK 100.00MHz (0.00% SSC)

*v008:*
* + updated the logo to the official one (taken from the new BIOS version) and enabled its display by default
* + fixed an issue with the PCI-E bus when it was running in 1.1 mode on some video cards *thanks to Snooki Lowe*
* + microcodes for V3 and V4 have been updated to the latest versions
* + version with disabled beeper is also available
* added +3.3V to HardwareMonitor
* BIOS base GHX99015
* ASPM support included
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu items "Memory Frequency" and "OverClocking Feature" will no longer disappear
* menu items "CPU C State Control", "Program PP0_CURT_CFG_CTRL_MSR", "SOCKET RAPL Config", "Per-Socket Configuration" and "PCI Subsystem Settings" are open
* BCLK 100.00MHz (0.00% SSC)

*v007:*
* + microcode for V4 and Realtek UNDI Driver updated to the latest versions
* + menu items "SOCKET RAPL Config", "Per-Socket Configuration" and "PCI Subsystem Settings" are open *thanks Pavlon and MacArrow*
* added +3.3V to HardwareMonitor
* BIOS base GHX99015
* ASPM support included
* the "OverClocking Feature" menu item will no longer disappear
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* the "Memory Frequency" menu item will no longer disappear
* menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v006:*
* + added +3.3V to HardwareMonitor
* + BIOS base GHX99015 *thanks v111*
* + ASPM support enabled
* + the menu item "OverClocking Feature" will no longer disappear *thanks Vitaliy Pukhov*
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* the "Memory Frequency" menu item will no longer disappear
* menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v005:*
* + updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, removed unnecessary stuff (Matrox GOP and Intel Gbit) *thanks v111*
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed BIOS date in its settings
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* the "Memory Frequency" menu item will no longer disappear
* menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v004:*
* + configured CPU fan speed control (<45°=30%/>80°=100%) *thanks mozg13 and v111*
* + fixed BIOS date in its settings
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* the "Memory Frequency" menu item will no longer disappear
* menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v003:*
* + menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* + menu item "Memory Frequency" will no longer disappear
* menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v002:*
* + menu item "CPU C State Control" is open
* BCLK 100.00MHz (0.00% SSC)

*v001:*
* + BCLK 100.00MHz (0.00% SSC) *thanks iEngineer*