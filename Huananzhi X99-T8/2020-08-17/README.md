### Huananzhi X99-T8
###BIOS 2020/08/17 (G3X99904)
Known changes compared to version 2020/05/25:

+ The beeper beeps more pleasantly
+ Intel Management Engine Interface disabled
+ Reduced the amount of hardware reserved RAM by 73.6MB
+ Added voltage readings on the +12V and +5V lines (in Hardware Monitor)
- ECC disabled (currently unknown how to fix it)
- No power saving state Package C6 (currently unknown how to fix)
- Removed the option to configure RAM timings (fixed in v001)
- Huananzhi engineers made a mistake in the DevicePathDxe module (fixed in v004)

*v006:*
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, tidied up SATA RAID drivers *thanks v111*
* access to CPU_FAN2 speed settings is now available (0=0%/255=100%)
* configured CPU fan speed control (<45°=30%/>80°=100%)
* fixed bug in DevicePathDxe module
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)

*v005:*
* access to CPU_FAN2 speed settings is now available (0=0%/255=100%)
* configured CPU fan speed control (<45°=30%/>80°=100%) *thanks mozg13 and v111*
* fixed bug in DevicePathDxe module
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)

*v004:*
* fixed bug in DevicePathDxe module *thanks iEngineer*
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)

*v003:*
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)

*v002:*
* access to timing settings is now available (item name "Memory Timings & Voltage Override") *thanks Vladimzam*
* BCLK 100.00MHz (0.00% SSC)

*v001:*
* BCLK 100.00MHz (0.00% SSC)
* access to setting timings is now available (item name "Memory Frequency") *thanks VK239*