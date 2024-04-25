### Machinist X99-K9
###BIOS 2020/06/03 (AAX99018)

+ ECC is active for server memory
+ There is an option to configure RAM timings
+ Quad-channel memory mode works on all processors
- Resetting settings with a jumper does not work, i.e. If you set settings that are incompatible with starting the system, you will have to sew with a programmer
- Starting the system without a video card does not work

*v004:*
* + microcode for V4 and Realtek UNDI Driver updated to the latest versions
* + menu items "SOCKET RAPL Config", "Per-Socket Configuration", "PCI Subsystem Settings" and "OverClocking Feature" are open
* updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, tidied up SATA RAID drivers
* access to timing settings is now available (item name "Memory Timings & Voltage Override")
* BCLK 100.00MHz (0.00% SSC)

*v003:*
* + updated microcodes and Realtek Boot Agent GE, added Realtek UNDI Driver, tidied up SATA RAID drivers
* + access to timing settings is now available (item name "Memory Timings & Voltage Override")
* + BCLK 100.00MHz (0.00% SSC)

Flash using afudos or afuwin with the /gan key

There is also [BIOS from iEngineer](https://github.com/BIOS-iEngineer/MACHINIST-X99ZV102/releases/latest). A jumper reset works with it, and the system is also functional without a video card. But on some processor models, for example E5-2678v3, quad-channel memory mode does not work.