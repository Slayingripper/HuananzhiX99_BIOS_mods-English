### Huananzhi X99-8M
###BIOS 2020/05/25 (GHX99015)

+ When using server (ECC) memory, error correction function is active
+ Timing Command Rate (CR) can take any specified value from 1 to 3

[To remove beeper signals](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods#%D0%9E%D1%82%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0% BD%D0%B8%D0%B5-%D0%B1%D0%B8%D0%BF%D0%B5%D1%80%D0%B0), just disable the code only in the Bds module

This BIOS is compatible with [Ultimate Patcher Tool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods#Ultimate-Patcher-Tool)

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