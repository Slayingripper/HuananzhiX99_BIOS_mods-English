Erying 11gen

A free assembly, no links, no advertising. Adequate price up to 13000 rub. for the option with i7-11800H or higher (April 2023), you can then consider something on the usual i5-12400 and the usual mother.

The ES 11800H differs from the ES 11980HK only by the overclocking potential. Both have a free multiplier. The first stability at 4.60GHz on average, the second at 4.80GHz. But in general, it depends on the copy.

In the list of files there are bioses: from Erying 111 and 307, and the so-called graphic bios with zippers (10729). It is known that 307 bios can octopus the fee on which the bios 111 works and vice versa. Also, the biosyp is compatible with 111 bios and bricks those boards that only 307 works.

The most important thing to do is to solve the problem with overheating of the processor. Whatever the thermopaste used between the chip and the plate, it was overheating. The liquid metal put everything back to normal. I mean, I.e. it was a cTB > ff > plate > paste > cooling. There is no more overheating, 75 in AIDA64 on one Stress FPU checkline.

1. [If the system freezes](If-free-systems)
2. 2. [Whether virtualization is working](Works-li-virtualization)
3. [How to set up TDP](How-configure-TDP)
4. [How to set up multipliers](How--configure-multipliers)
5. [How to make undervolt](How-to make-undervolt)
6. [How to enable built-in video when using a video card](How-on-on-enabled-built-in video-use-video card)
7. [Where to take the drivers](Where-take-drivers)
8. [How to configure RAM](How--configure-operational memory)
9. [How to enable ReBAR](How--Off-ReBAR)
10. [If RGB control does not work on memory](?If-non-work-work-management-RGB-on-memory)
11. [How to flash the programmer](How-Fake-programmer)

***[> Telegram Group](https://t.me/russian_xeon_community) ***

If the system freezes

This is expressed in the hanging of the image on the screen, while the system continues to work. In my case, this happened when the combination of a high load on the processor with its high temperature, after a while. For example, from 80o at 60W or from 70o at 90W.

This only happens if the video card uses the PCI-E bus in 1.0(1.1). On my Radeon RX 570 there is no such problem, the tire is constantly held in 3.0 mode. On the GeForce RTX 3070 tire in a simple fall to 1.1 and the problem may arise.

You can fix the lower limit of the bus through [NVIDIA PMM Tool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/blob/master/Erying%2011gen/NVIDIA_PMM_Tool_vvv2.5.0.120_20230427.zip), there is no problem in PCI-E 2.0. And it works only with the RTX 30 series. If it works on other series, please write off in [our Telegram group](https://t.me/russian_xeon_community).

To do this, run NVPMM.exe, on the Control tab, put the Adaptive VRAM bottom check, specify the process in which it will work, for example, explorer.exe, and the minimum memory frequency of 810MHz. And after that, for example, in [GPU-Z](https://www.techpowerup.com/download/techpowerup-gpu-z/) make sure the minimum threshold rises to 2.0. The freezing must stop.

In general, it is believed that the problem occurs only in combination with NVIDIA. There is no more beautiful solution to the problem at the moment. If you find a more elegant solution to this problem, please write off in [our Telegram group](https://t.me/russian_xeon_community).

Does virtualization work?

Virtualization works, for example in VirtualBox and BlueStacks

But for some reason, the Hyper-V system component does not work. When activated, the system is rebooted at the loading stage. Helps turn off virtualization and then disconnect Hyper-V in the system. For the same reason, the "Isolation of the core" does not work.

Configuring Virtualization - CPU Configuration > Intel (VMX) Virtualization Technology

How to set up TDP

You can configure TDP, for your cooling system, or remove limits - Power & Performance > CPU - Power Management Control > View/Configure Turbo Options > Power Limit 1 Override > Enabled. Next, enter in Power Limit 1 and 2 the value of the desired TDP in the millitrates, i.e. for 45W we enter 45000.

How to set up multipliers

In the menu of Power & Performance > CPU - Power Management Control > View/Configure Turbo Options > Core Turbo Ratio Ratio (TRLR) Override enter the desired multipliers (for example, maximum)

OverClocking Performance Menu > OverClocking Feature > Enabled, hereinafter Processor > Per Core Ratio Override > Enabled, then enter the multipliers in the Core Max OC Ratio and each Core Max Ratio

How to make an undervolt

OverClocking Performance Menu > OverClocking Feature > Enabled, hereinafter Processor > Core Voltage Offset Prefix put on "-" and in Core Voltage Offset we enter the desired displacement in the miles, for example 50

I recommend testing the stability in [OCCT](https://www.ocbase.com/) with the following settings:

- Tab: CPU
- Dataset: Large
- Mode: Heavy
- Load: Variable
- Instructions: SSE (not AVX)
- Flows: Auto

How to enable built-in video when using a video card

System Agent (SA) Configuration > Graphics Configuration > Internal Graphics > Enabled

Where to get drivers

On this page [developed](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/blob/master/Erying%2011gen/drivers_erying11gen.zip) drivers for:

- Intel SMBus (to install, click PCM by tigerlakepch-hsystem.inf and select "install")

- other unknown devices in Device Manager (HM570_serialIO.exe)

for built-in graphics current driver on [Intel](https://www.intel.ru/content/www/en/en/download/726609/intel-arc-iris-xe-graphics-whql-windows.html) , and you can download from [TechPowerUp](https://www.techpowerup.com/down/intel-graphics-drivers)

How to set up RAM

System Agent Agent (SA) Configuration > Memory Configuration > Sets the gear ratio when SAGV is disabled > put "1," to achieve the best latency, or "2" to increase the acceleration capacity of memory

System Agent (SA) Configuration > Memory > Memory > Memory > Memory profile, select your XMP or Custom (manual configuration)

Custom profile is better run with a voltage of 1.20V, and then, after a successful start, if necessary, increase the voltage to 1.35V. Otherwise, the system may not start at 1.35V.

To take frequencies higher than 3200, it may be necessary to increase the voltage of Uncore

My results are so (memory 2pcs. Crucial Ballistix BL16G32C16U4BL.16FE:

3333MHz 16-18-18-36 / Uncore+50mV

3466MHz 16-18-18-36 / Uncore+100mV

3600MHz 16-19-19-36 / Uncore+170mV (Adult in test AIDA64 about 56000/52500/53000/62ns)

Stability check in normal tests, for example [testmem5 with Extreme1 profile ?anta777](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/bblob/master/TM5.zip)

How to enable ReBAR

PCI Subsystem Settings - Re-Size BAR Support

If RGB control does not work on memory

You need to install the driver on the Intel SMBus device

How to flash the programmer

If the mat. plat is mounted in the hull, then most likely it will have to be retrieved, because. The pliny of the programmer will interfere with the radiator of the hub, and in order to remove it, you need to pull out the back of the lulls. Be careful and do not overwhelm the radiator on the hub, so as not to grind it. The paste does not need to be changed, thermal gaskets, too, because. there is a good thermal interface with phase transition.

You can also avoid all this if you modify the peg, namely to rip one of its sides.

Maybe the problem with the contact fishing pinchet, but you can catch it. Hash through [NeoProgrammer](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/blob/master/NeoProgrammer_2.2.0.10.zip).