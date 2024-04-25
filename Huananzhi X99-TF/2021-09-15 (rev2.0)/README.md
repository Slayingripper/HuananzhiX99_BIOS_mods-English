### Huananzhi X99-TF
###BIOS 2021/09/15 (G3X99911)

The Command Rate (CR) timing has a value of 3 and does not change in any way in the settings (at the moment it is not known how to fix it)
As before, when using server (ECC) memory, the error correction function is not available (active from BIOS version 2021-12-13)

Known changes compared to version 2021/05/11:

+ New brand logo at system launch

*v001:*
* microcodes updated
* fixed an issue with the PCI-E bus when it was running in 1.1 mode on some video cards *thanks Snooki Lowe*
* configured CPU fan speed control (<45°=30%/>80°=100%)
* menu items "CPU C State Control", "SOCKET RAPL Config", "Per-Socket Configuration", "OverClocking Feature", "Program PP0_CURT_CFG_CTRL_MSR" and "PCI Subsystem Settings" are open
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)