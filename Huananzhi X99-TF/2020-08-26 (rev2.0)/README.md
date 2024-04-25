### Huananzhi X99-TF
###BIOS 2020/08/26 (G3X99905)

As before, when using server (ECC) memory, the error correction function is not available (active from BIOS version 2021-12-13)

Known changes compared to version 2020/08/17:

+ Huananzhi engineers have fixed a bug in the DevicePathDxe module
- Command Rate (CR) timing has a value of 3 and does not change in any way in the settings (at the moment it is not known how to fix it)

*v001:*
* menu item "Program PP0_CURT_CFG_CTRL_MSR" is open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)