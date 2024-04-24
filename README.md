***[> Telegram Group](https://t.me/russian_xeon_community) ***

***[> Discord server](https://discord.gg/mRNBU5YpzW)***

***[> VK Community X99](https://vk.com/koshak1013)***

***[> VK Community X79](https://vk.com/huanan_x79)***

The Table of contents

1. [Unlock (Russian)](instruction-on-unlock-maxofrecks-on-all-core-a-na-na-on-on-two-unlock), [Unlock (English)](instruction-for-sexco-on-frequency-all-core-not-two-unlocked](instruction-on-serfrequency-all-core-not-two-unlock](instruction-for-s]
2. 2. [Undervolting (Russian)](selection-optimal-meaning-shift-stension-on-our-processor-undervolting), [Undervolting (English)](finding-the-optimal-voltage-offset-values-for-your-processor-undervolting)
3. [Unlock and Undervolting with the Ultimate Patcher Tool](ultimate-patcher-tool)
4. [Restoration of the bios by the programmer](Repair-bios-programmer)
5. [Configuration of RAM timing](configuring-type-tyming-operation-memory)
6. [What to do if system load is lost](them-to do-if-defeat-down-down-system)
7. [How to open the hidden menu items of bios](k-open-hidden-point-menu-bios settings)
8. [Adding support for Resizable BAR in bios](Approval-support-resizable-bar-in-bios)
9. [Disconnect the beeper](disconnect-beper)
10. [Frequently asked questions](of frequently asked-questions)
11. [On post-codes](o-post-codes)
12. [If you observe the frequency of the system tyre less than 99.75MHz](if-you-observe the-frequency-system-tire-thick-lesser than 9975mgts)
13. [Funator speed control settings for Huananzhi X99-8M/8MD/8/F8/TF](configuration-management-turn-fventvor-for-huananzhi-x99-8m8md3f8tf)
14. [If you have a socket damaged](if-u-vas-damaged-sooked)

Instructions for unlocking the max.frequency on all kernels, not on two (unlock)

Before you start, make sure you are using the [relevant version of S3TurboTool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/master/S3TurboTool_v1.53cat_S3THv1_DXETHV1_RAWTH1v.rar)

*(for this utility and new unlock driver special thanks ***ser8989***)*

1. Run S3TurboTool and press MMTool5
2. 2. In the existing utility "MMTool Aptio" press "Load Image" and choose the necessary bios
3. Go to the "CPU Patch" tab, allocate the microcode "6F 06F2," note "Delete a Patch Data," click Apply and agree
4. Click "Save Image" and close "MMTool Aptio"
5. In S3TurboTool press AMIBCP
6. In the available AMIBCP utility, open a bios
7. Open the list and go the way "Common RefCode Configuration > IntelRCSetup > Advanced Power Management Configuration > CPU C State Control" (the way may differ on branded motherboards)
8. On the right, in the column Optimal, double-click change the value of parameters:
    * "Package C State limit" on "C2 state"
    * "CPU C3 report" on "Enable"
    * "CPU C6 report" on "Disable"
9. Close the AMIBCP window and agree to save the changes
10. ***If the system is two-processor, then proceed to the creation of a DXE driver. For single-processor systems, you need to check if our biosayer has a PchS3Peim module.*** In S3TurboTool, press UEFITool.
11. In the UEFITool utility, we open a bios
12. Open the list and go on the way "Intel image > BIOS region > 8C8CE578-...(the lowest in which PEI drivers) >"
13. About the first 20 values are we looking for 271DD6F2-... (PchS3Peim module). If there is one, we will collect a PEI driver. If not, we'll collect the DXE driver.

"details>
"summary>PEI driver" /summary>

(supports sleep mode, supports only single-processor systems, does not support branded motherboards):
1. In S3TurboTool click "Assembling the driver"
2. 2. Configure the necessary voltage offsets ([method of finding approximate values](Sample-optimal-meaning-shift-voltages-voltage-on-processor-undervolting) Also choose whether an additional signal is needed when you turn on and output the system from sleep. Click "Assemble Driver."
3. In S3TurboTool press UEFITool
4. In the UEFITool utility, we open a bios
5. Open the list and go on the way "Intel image > BIOS region > 8C8CE578-...(the lowest in which PEI drivers) >"
6. We find 271DD6F2-... (PchS3Peim module)
7. Right click on it, click "Replace as is...," select the previously assembled driver (is in the folder S3TurboHack)

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/ra/master/.git_images/01/png)

8. Choose "File > Save image file...," save. Bios ready for firmware. You can also flash the appropriate button in the S3TurboTool.

* If an error 103 occurs when trying to firmware, you should reboot the system.*

*If your own or someone else's dump was used to modify the bios, then after the firmware, you need to reset the bioss settings to the standard (in the menu of bios settings or bar).*
?/details>

"details>
"summary>DXE driver . . . . . . . . . . . . . . 

(Do not support sleep mode, supports both one- and two-processor systems, sleep will work on the two-processor system, supports ASRock and GIGABYTE boards):
1. In S3TurboTool click "Assembling the driver"
2. 2. Click in the upper right corner of the DXE button
3. Configure the necessary voltage offsets ([method of finding approximate values](Sample-optimal-meaning-shift-voltages-voltage-on-processor-undervolting) Also choose whether you need an additional signal when you turn on. Click "Assemble Driver."
4. In S3TurboTool press UEFITool
5. In the UEFITool utility, we open a bios
6. Open the list and go on the way "Intel image > BIOS region > 8C8CE578-...(the penultimate, second bottom, in which DXE drivers) >"
7. Scroll to the bottom and find the latest DXE driver in the list
8. Right click on it, click "Insert after...," select the previously assembled driver (is in the folder DXETurboHack)

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/git_images/screen02.png)

9. Choose "File > Save image file...," save. Bios ready for firmware. You can also flash the appropriate button in the S3TurboTool.

* If an error 103 occurs when trying to firmware, you should reboot the system.*

*If your own or someone else's dump was used to modify the bios, then after the firmware, you need to reset the bioss settings to the standard (in the menu of bios settings or bar).*
?/details>

"details>
"Summary>RAW driver" /summary>

(supports sleep mode, supports only single-processor systems, does not support an angle of AVX mode):

***Chinese motherboards do not need this driver and it is not recommended for them to do unlock in this way. Only for extreme cases, for unusual branded motherboards.***

* ATTENTION! After installing the driver RAW, do not edit this bios with any programs, otherwise the bios will become inoperable.*
1. In S3TurboTool click "Assembling the driver"
2. 2. Click in the upper right corner of the RAW button and choose the necessary bios
3. Configure the necessary voltage displacements. Click "Assemble and install the driver."
4. The bios is stored in the same folder and is ready for firmware. You can also flash the appropriate button in the S3TurboTool.

* If an error 103 occurs when trying to firmware, you should reboot the system.*

*If your own or someone else's dump was used to modify the bios, then after the firmware, you need to reset the bioss settings to the standard (in the menu of bios settings or bar).*
?/details>

***If you have any difficulties, as well as if you have comments and wishes, please contact [Telegram group](https://t.me/russian_xeon_community)***

[Video instruction](https://youtu./2befhhdrIrXR4) *(thanks to Zerg_fb)*:

[![](https://i.ytimg.com/vi/2hfhdrhIrXR4/mqdefault.jpg](https://youtu.be/2hfhdrIrXR4)

Instructions for unlocking the maximum frequency for all cores, not two (unlock)

Make sure you are using the [latest version of S3TurboTool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/ra/master/S3TurboTool_v1.53cat_S3vton_DXETH1_RAWTHv1_RAWTHv1b.rar) before the starting.

* * Special thanks to ***ser898989*** for this utility and the new unlock driver)

1. Launch S3TurboTool and click MMTool5
2. 2. In the recipe utility "MMTool Aptio," click "Load Image" and select the required BIOS
3. Go to the "CPU Patch" tab, select the "6F 06F2" microcode, mark "Delete a Patch Data," click Apply and agree
4. Click "Save Image" and close "MMTool Aptio"
5. In S3TurboTool, AM clickIBCP
6. In the available AMIBCP, open the BIOS
7. Expand the list and follow the path "Common RefCode Configuration > Advanced Power Management Configuration > CPU C State Control" (the path may differ on branded motherboards)
8. On the right, in the Optimal column, double-click to change the value of the parameters:
    "Package C State limit" to "C2 state"
    * "CPU C3 report" to "Enable"
    * "CPU C6 report" to "Disable"
9. Close the AMIBCP window and agree to save the changes
10. If the system is dual-processor, then to make the proceed DXE driver. For uniprocessor systems, you need to check if there is a PchS3Peim module in our BIOS.*** In S3TurboTool, click UEFITool.
11. In the UEFITool utility that appears, open the BIOS
12. We open the list and follow the path "Intel image > BIOS region > 8C8CE578-...(the lowest one, in which the PEI drivers)
13. We are looking for 271DD6F2-... (PchS3Peim module) among the first 20 values. If there is one, then we will build the PEI driver. If this is not the case, then we will build the DXE driver.

"details>
"summary>PEI driver" /summary>

(supports sleep mode, only supports uniprocessor systems):

1. In S3TurboTool, click "Assembly driver"
2. 2. We adjust the voltage offset required offsets ([method for approximate finding values]];Finding-the-optimal-voltage-offset-value-for-your-processor-undervolting). We also choose whether an additional signal is needed when turning on and waking the system from sleep. Click "Assemble a driver."
3. In S3TurboTool, click UEFITool
4. In the UEFITool utility that appears, open the BIOS
5. We open the list and follow the path "Intel image > BIOS region > 8C8CE578-...(the lowest one, in which the PEI drivers)
6. Find 271DD6F2-... PCHS3Peim module
7. Right click on it, click "Replace as...," select the previously assembled driver (located in the S3TurboHack folder)

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/ra/master/.git_images/01/png)

8. Choose "File > Save image file...," save. BIOS is ready for flashing. You can also flash it with the corresponding button in S3TurboTool.

*If error 103 occurs when trying to flash, then you should reboot the system.

*If you used your own or someone else's dump to modify the BIOS, then after flashing, you need to reset the BIOS settings to the minimum standard (in the BIOS menu settings or using a jumper).
?/details>

"details>
"summary>DXE driver" /summary>

(does not support sleep mode, supports single and dual processor systems):
1. In S3TurboTool, click "Assembly driver"
2. 2. Press the DXE button in the upper right corner
3. We adjust the voltage offset required offsets ([method for approximate finding values]];Finding-the-optimal-voltage-offset-value-for-your-processor-undervolting). We also choose whether an additional signal is needed when needed turning on. Click "Assemble a driver."
4. In S3TurboTool, click UEFITool
5. In the UEFITool utility that appears, open the BIOS
6. Expand the list and follow the path "Intel image > BIOS region > 8C8CE578-...(penultimate, second from the bottom, in which DXE drivers)
7. Scroll to the bottom and find the last DXE driver in the list
8. Right click on it, click "Insert after...," select the previously assembled driver (located in the DXETurboHack folder)

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/git_images/screen02.png)

9. Choose "File > Save image file...," save. BIOS is ready for flashing. You can also flash it with the corresponding button in S3TurboTool.

*If error 103 occurs when trying to flash, then you should reboot the system.

*If you used your own or someone else's dump to modify the BIOS, then after flashing, you need to reset the BIOS settings to the minimum standard (in the BIOS menu settings or using a jumper).
?/details>

"details>
"SUMMARY>RAW driver" / / summary>

(supports sleep mode, only supports uniprocessor systems, does not support AVX mode unlock):

***Chinese motherboards do not need this driver and it is not recommended to unlock them in this way. Only as a last resort, for unusual branded boards.***

*ATTENTION! After installing the RAW driver, do not edit this BIOS with any programs, otherwise the BIOS will become inoperable.*
1. In S3TurboTool, click "Build Driver"
2. 2. Press the RAW button in the upper right corner and select the required BIOS
3. Adjust the voltage required offsets. Click "Assembly and install the driver."
4. The BIOS is saved in the same folder and is ready for flashing. You can also flash it with the corresponding button in S3TurboTool.

*If error 103 occurs when trying to flash, then you should reboot the system.

*If you used your own or someone else's dump to modify the BIOS, then after flashing, you need to reset the BIOS settings to the minimum standard (in the BIOS menu settings or using a jumper).
?/details>

***If you have any difficulties, as well as if you have comments and suggestions, please contact the [Tele group](https://t.m/russian_xeon_community)***

Selection of optimal stress offset values on your processor (undervolting)

**First learn the theory, then go to the instruction!**

As you know, China boards do not allow adequately, in its usual form, to change the voltage of the processor for 26xx v3 (46xx v3) systems. When using turbobust unlock, a voltage reduction is used to make the processor work longer or at a higher frequency. But the reduction of the offset voltage occurs simultaneously in all modes (there are more than three of them). And the most problematic part is the tension in a simple. Thus, when selecting an unlock driver with numbers, for example, "V3_MOF_705050.fss" there is a reduction in the power supply voltage of the processor by 0.07V in all modes of operation, a decrease in the cache of the processor by 0.05V in all modes of operation. Experience has shown that instability, in the vast majority of cases, is manifested in a state of system downtime (inaction). Thus, you can without the use of unlock, in normal mode, reduce the frequency of the processor offset and conduct testing, without fear of the firmware of the biospot and similar problems. And in the future, when the processor downtime is known, reduce them once and for all with the biosom with the help of the program (S3TurboTool Sergey Bakaev ser8989). The change will occur using the software and when the system hangs or the appearance of BSOD after rebooting everything will return to the original state.

Several programs are suitable to change the voltage. Intel XTU, QuickCPU and ThrottleStop. In general, the instruction is this: reduce the voltage of the processor, test different programs in the load, if well, then we leave for long-term use. Typically, a working decline will be considered from 40 to 90, depending on the processor model and the specific instance. (For L processors can be a worker and 120).

In the second step, reduce the voltage on the Cache cache. Usually in drivers, the value of 50-60 is selected, but in practice it can easily exceed 120. Instability to check LinX with AVX instructions and programs that compress memory (for example TestMem5).

After finding the values at which the system is stable in both simple and load, you can flash these values into the motherboard bios board.

*(author ***Vasily Pupkin***)*

----

Each processor model has a TDP value, which is its maximum power in watts. In some tasks, this limit is achieved, and the processor begins to reduce the frequency on the cores with steps of 100MHz, so as not to cross this line. Power, it is a voltage multiplied by current. Lowering voltage, improved energy efficiency of the processor, i.e., improvement of the energy efficiency of the processor is achieved. at the same load reduces energy consumption and, as a result, heat dissipation. Accordingly, at the same boundary load, the processor will be able to more confidently hold the frequency.

We will touch two blocks in our processors - Core (cores) and Cache (cache) (there is also a SystemAgent block, but a reduction in the voltage does not reduce the consumption of the processor, so it is better not to change it).

The voltage is reduced by the method of its offset (offset) by a certain amount. I-e.e. in all processor modes, the voltage will be less on the value we set. You can safely search for offset values on the kernels on a system without unlock. You can do this on a system with active unlock, in this case, when changing the displacement, the unlock will disappear. This will not affect the search for meaning, because. The voltage in the cores varies depending on its frequency.

***Before further actions, save important data in your system, be prepared for possible hangouts or blue screen!
Before running the tests, take care of the proper cooling of the processor, the VRM area and RAM (it can rotate without additional cooling)!

1. Preparation: download the necessary programs - to change the voltage offset we will use [ThrottleStop](https://www.techpowerup.com/download/techpower-throttletop/), to test the stability of the cores - the program [OCCT](https://www.ocbase.com/download), for cache stability test - [LinX v0.6.5](https://www.s.

* Selection of optimum value of offset voltage to core**

1. Run ***ThrottleStop***, click ***FIVR***
2. 2. In the block ***FIVR Control*** we celebrate ***CPU Core***
3. In the block ***CPU Core Voltage*** *** we note ***Unlock Adjustable Voltage***, lowering ***Offset Voltage***, start with ***-100mV*** and press ***Apply***. If the system is hovering or we saw a blue screen, then such a shift does not suit us, reboot the system and try -95mV, -90mV, etc.
4. If everything seems to be stable, then we run ***OCCT***, put the test mode:
    - Tab: CPU
    - Dataset: Large
    - Mode: Heavy
    - Load: Variable
    - Instructions: SSE (not AVX)
    - Flows: Auto

5. We're running the test. If the system is hovering or we see a blue screen (usually the CLOCK_WATCHDOG_TIMEOUT error), then we reduce the offset and continue to test until stability (***1 hour***). This will be our importance for the cores.

**Selection of optimal voltage offset value to cache**

1. Run ***ThrottleStop***, click ***FIVR***
2. 2. In the block ***FIVR Control*** celebrate ***CPU Cache***
3. In block ***CPU Cache Voltage*** *** we note ***Unlock Adjustable Voltage***, lowering ***Offset Voltage***, start with ***-125m*** and press ***Apply***. If the system is hovering or we saw a blue screen, then such a displacement does not suit us exactly, reboot the system and try -120mV, -115mV, etc.
4. If everything seems to be stable, then we run ***LinX***, configure the test:
    - Memory: 8192MB (or less if free memory is less)
    - Perform: 10 minutes

5. We're running the test. In case of instability, a blue screen is possible (usually the error ***WHEA_UNCORRECTABLE_ERROR***), if this happens, then reduce the displacement and continue to test until stability. This will be our value for cache.

That's because. for cache checking dense data streams are needed, then it is recommended to conduct a test again, but with an unlock together with the SVID/FIVR bump (pay special attention to the temperature during the test)

*(help in the preparation of the instruction ***Data Name ID***)*

Finding the optimal offset values for your processor (undervolting)
----
As you know, China boards do not allow adequate toly, in the usual form, change the processor voltage for 26x v3 (46x v3) systems. When using a turbo-boost unlock, a voltage reduction is used to make the processor work longer or at a frequency higher. But voltage reduction by offset simultaneously recovering in all modes (there are more than three of them). And the most problematic is a stress in idle time. "Well, when selecting an unlock driver with numbers," for example "V3_MOF_705050.fss," the processor voltage decreases by 0.07V in all operating modes, the processor cache decreases by 0.05V in all operating modes. Experience has shown that instability, in the overwhelming majority of cases, manifests itself in a system idle state (inactivity). That, it is possible, without using an unlock, in the normal mode, to reduce the frequency processor by offset and conduct testing without fear of BIOS firmware and related similar problems. And in the future, when the processor idle operating voltages are known reduce them once and for all by the BIOS using the program (S3TurboTool Sergey Bakaev ser898989). The change will happen with the help of software, and when the system hangs or reboots, everything will return to its original state.

Several programs are suitable for changing the voltage. Intel XTU, QuickCPU and ThrottleStop. In general, the instruction is as follows: we lower the processor voltage, test it with programs in the load, if it is good, then we leave it for long-term use. Typically, a working degradation will be considered from 40 to 90, depending on the processor model and specific instance. (for L processors, 120 can be working).

The second step is to lower the voltage on the processor cache. Usually the driver choose a value of 50-60, but in practice it can easily exceed 120. Check the instability with the LinX program with AVX-instructions and programs that are heavily load memory (for example TestMem5).

After finding the values that system stably works stably both in idle and in load, that values can be flashed into the BIOS of the motherboard.

*(by ***Vasily Pupkin***)

----

Each processor model has a TDP value, this is its maximum power in watts. In some tasks, this limit is reached, and the processor begins to reduce the frequency on the cores in steps of 100MHz in order not to go beyond this limit. Power is voltage times current. Lowering the voltage improves the processor's energy efficiency, i.e. at the same load, energy consumption, as a a consequence, heat generation are reduced. Accordingly, with the same boundary load, the processor will be able to hold the frequency more confidently.

Let's touch on two blocks in our processors - Core and Cache (there is also a SystemAgent block, but lowering the voltage on it does not reduce the processor consumption, so it is better not to change it.

The voltage is lowered by offsetting it by a certain amount. That is, in all operating modes of the processor, the voltage will be less by the value set by us. It is safe to search for bias values on the cores on a system without unlock. You can do this on a system with an active unlock, in which when the offset is changed, the unlock will be released. This will not affect the search for a value in any way. in nuclei, the voltage changes depending on its frequency.

To change the offset, we use the Intel XTU, QuickCPU or ThrottleStop program. Further it will be considered on the example of the last.

Before proceeding, save important data on your system, be prepared for free possibleze or blue screens.
1. After launching [ThrottleStop](https://www.techpowerup.com/download/techpowerup-throttlestop/), press FIVR
2. 2. In the "FIVR Control" block, "CPU Core" is marked, which means we change the offset on the cores
3. In the "CPU Core Voltage" block, select "Unlock Adjustable Voltage," lower the "Offset Voltage," for example, to -100mV and click Apply. If the system freezes or we see a blue screen, then such an offset is definitely not suitable for us, we reboot the system and try -95mV, etc.
4. If everything seems to be stable, then we launch the [OCCT](https://www.ocbase.com/), set the test mode "CPU/Data set Large/Mode Extreme/Load type Variable/Intrainstru set SSE/Threads Auto." Why SSE and not AVX? Because under AVX load, the processor switches to another operating mode, adds voltage and decreases frequency. This will not work when testing the stability of the cores. Before running the test, we take care of proper cooling of the processor, VRM area and RAM (it can throttle without additional cooling).
5. We run the test. If the system freezes or we see a blue screen (usually the CLOCK_WATCHDOG_TIMEOUT error), then we reduce our offset and continue to advance before the stability (1 hour). This will be our core value.

Next, we move on to the cache test (you can start with -125mV) Optimally test the cache in LinX (tested on [v0.6.5](https://github.com/sanekgusev/LinX-old/releases/latest), set the 8192MB setting memory, press. In case of instability, a blue screen is possible (usually a WHEA_UNCORRECTABLE_ERROR error). 5 minutes of the test is enough.

Because to check the cache, dense data streams are needed, then it is recommended to run the test again in the future, but this time with unlock, coupled with the SVID/FIVR bug (pay special to attention the temperature during the test)

The Ultimate Patcher Tool

In April 2021, the program [Ultimate Patcher Tool](https://nalex.me/ultimate-patcher-tool/) (fur UPT) for a more convenient process of bios for the purpose of unlock and undervolt and even to replace the logo. Also, on some bios, it is possible to eliminate the problem, because of which the smart fan did not work after the system returns from the sleep regime.

UPT supports loading the desired bios directly from the githabs, also offers to choose what exactly needs to be modified. If you can not choose to fix the smart fan, then this is not yet supported for the selected bios. Supports not only C612/X99 chipsets, but also others that are installed on the LGA2011-3 platform.

After the modification, the biosage must be flashed in any way (programmer, afuwin, fptw64, [S3TurboTool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/w/master/S3TurboTool_v1.53cat_S3THv1_DXETHV1_RAWVHV1r)

* ATTENTION! At the moment, the project is in the testing stage, so do not pose a modified bios if you do not have the opportunity to recover with the programr.

In the BIOS settings, usually in the IntelRCSetup section, there should be the "OverClocking Feature" menu, which will include the following menus:
- Processor > Core Voltage Offset (distance of cores in mV, pay attention to its prefix)
- CLR/Ring > CLR Voltage Offset (cache voltage offset in mV, pay attention to its prefix)
- Uncore > Uncore Voltage Offset (systemAgent voltage offset in mV, pay attention to its prefix)
- SVID/FIVR > SVID Support (disconnection is equivalent to "Bag SVID/FIVR" in S3TT)

Proven bioses:
- Huananzhi X99-8M/8MD3/F8/T8/TF (25.05.2020 - works) (17.08.2020 and newer - ! WORK! - Post code 79)
- Huananzhi X99-F8D/T8D (24.06.2020 - everything works except the smart fan)
- Jginyue X99M-PLUS D3 (03.11.2020 - everything works, except for the smart fan)

The list will be replenished, report the results to [Telegram group](https://t.me/russian_xeon_community)

Rehabilitation of the bios by the programmer
The processor, RAM and the CR2032 power supply optionally be retrieved. In some cases, a connected PD is necessary, for duty voltage (the system must be turned off at the same time).

Huananzhi X99-F8/T8/TF is required to extract from the body, and remove the radiator from the hub, as it is required. It is attached with screws from behind.

Next, the instruction will be given on the example of the common programmer CH341A.

1. The pinch is inserted into the programmer, in the section for the 25 series of SPI chips, observing the key. The red wire should be in the same corner where the point on the chip image.
2. 2. Wear a peg on the chip itself, also observing the combination of the red wire with the dot on it.
3. Connect the programmer to the PC.
4. Download [NeoProgrammer](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/blob/master/NeoProgrammer_2.2.0.10.zip) and unpack the archive.
5. Go to Device Manager. We install the necessary drivers (select a folder with NeoProgrammer).
6. Run NeoProgrammer, click the icon with the question sign (Identify the chip). There must be a chip model. If there is no definition, we have poor contact with the chip (usually between the plinder and the chip). If successful, choose a model from the proposed list. Sometimes it's not the same, just pick something like that. Now we can read the contents of the bioscheme, if necessary, by clicking the "Read chip" icon. To save to the file, click the "Save file" icon.
8. For firmware, first erase the contents by clicking on the "Erase" icon. Next, open the working bioss file in the program and press the icon "Write." The firmware process can last from a few minutes to an hour.
9. After the firmware, I recommend you to read the contents of the bioscheme, save to the file, and compare with the original by the control amount.

Configuring RAM timings

[Video instruction](https://youtu.be/2UdU4n6B0V8). Recommended for development.

[![](https://i.ytimg.com/vi/2UdU4n6B0V8/mdefault.jpg)](https://youtu.be/2UdU4n6B0V8)

* thank you for Ilyme)*

There is also another instruction.

1. to fill as a konad
2. 2. open in aida64 SPD tab, take a screenshot, throw it in your favorites in a cart
3. open the same tab 1 below, screen, yourself
4. reduce by 1 first 3 times, reduce by 2, cache and memory test in the aide, remember the results and values of timings
5. repeat while the load is loaded, when not start, increase the first 3 back and reduce 1 only 4
6. intermediate execution, go to trfs
7. look there in the SPD of p2 the minimum value tRFC, add to it how many to the number of a multiple of 8, with another 8
8. to the minimum tRFC on the drug will start add another 8-16 and test the same in the aide cache and memory
9. set tREFI parameter to 32767 if your isn timings (first 3) odd, and 32760 if even
10. good to test in the aid
11. test in the memtest with a standard settings profile
12. test the stability of the system and for departures in games
13. as a kadna, maximum performance

*(author ***KOT JIETA***)*

**Quick stability test.**

**If after the modification of timing the system does not start, then reset CMOS by jumper.**

**If the start was successful, then check the amount of memory. If it is reduced, the configuration is unstable. If everything is ok, we run [testmem5 with Extreme1 profile *anta777](https://github.com/Koshak1013/HuananiX99_mods/blob/master/TM5.zip) and wait at least 20 minutes.**

You can ask any question that has arisen for overclocking the memory in [Telegram group](https://t.me/russian_xeon_community)

What to do if the system load is lost

You can face this problem if the system is installed on a disk with a GPT partition style. Usually, after resetting the bios), the first load is carried out normally, and after the reboot, we see an error, because. The loader is completely gone.

To solve this problem, go to the "Advanced > CSM Configuration" menu and change the value of the item "Boot option filter" to "UEFI only"

![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/.gitimages/screen11.png)

How to open hidden bios are menu items

To do this, you will need AMIBCP (available as part of [S3TurboTool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/master/S3TurboTool_v1.53cat_S3THv1_DXETH1_RAWTHv1.rb.rar)

We open a bios file in it and see the menu structure. We find the necessary hidden menu item and change the value of the parameter "Access/Use" from "Default" to "USER." If this section of the menu is also hidden, then go to the higher section and open access to it.

There is also [video instruction](https://youtu.be/BddkZIsLN_k)

[![](https://i.ytimg.com/vi/BddkZIsLN_k/mqdefault.jpg](https://youtu.be/BddkZIsLN_k)

Adding support for Resizable BAR to bios

1. Download [ReBarDxe.ffs and ReBarState.exe](https://github.com/xCuri0/ReBarUEFI/release/latest)
2. 2. Open in [UEFITool 0.28.0](https://github.com/LongSoft/UEFITool/releases/tag/0.28.0) bios file
3. Open the list and go on the way "Intel image > BIOS region > 8C8CE578-...(the penultimate, second bottom, in which DXE drivers) >"
4. Scroll to the bottom and find the latest DXE driver in the list
5. Right click on it, click "Insert after...," select the previously downloaded ReBarDxe.ffs file
6. Choose "File > Save image file...," save. We're in.
7. activate the setting of Above4GDecoding
8. From under Windows, run ReBarState.exe and enter two digits "32" and press the input. We're rebooting.
9. In [GPU-Z](https://www.techpowerup.com/download/techpowerup-gpu-z/) you can check the state of ReBar, including. fulfillment of each condition for activation

There is also [video instruction](https://youtu.be/CR7QV135ANw)

[!![](https://i.ytimg.com/vi/CR7QV135ANw/mqdefault.jpg)](https://youtu.be/CR7QV135ANw)

Disconnection of the bepper

***The old method, which is extremely rarely working, so I recommend you immediately contact [Telegram group](https://t.me/russian_xeon_community).***

1. We need certain modules from the biosand to get them to be opened [S3TurboTool](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/master/S3TurboTool_v1.53cat_S3vTH1_DXETHV1_RAWTHv1.b.arr), click on the UEFIOL
2. 2. Open the list and go on the way "Intel image > BIOS region > 8C8CE578-...(the penultimate, second bottom, in which DXE drivers) >"
3. In the right column itself there are module names, looking for Bds(stop from above) and StatusCodeDxe(s) search from below)
4. Right click on the "PE32 image section," click "Extract body...," save the module with the appropriate name, so as not to get confused. We also do the second module.

!![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/w/master/.git_images/03.png)

5. In S3TurboTool, click Beep in the upper right corner
6. Click the left icon to open the module file and select one of the modules
7. Click the right icon "Beep Off" and do the same with the second module
8. Now we open the UEFITool again (repeat the steps 1-3 instructions), make the right click on the "PE32 image section," click "Replace body...," and choose the appropriate module. We also do the second module.
9. Choose "File > Save image file...," save. Bios ready for firmware. You can also flash the appropriate button in the S3TurboTool.

*If the bepper still makes sounds, then try to process the StatusCodePei module (in the section with PEI modules).*

Frequently Asked Questions
----
***Question:*** What is the advantage of the new driver from S3TurboTool in front of payne and MOF drivers?

***Answer:*** The problem in which the unlock was dropped when the system was removed from the sleep regime. The power consumption of the processor without load was also reduced.

----
***Question:*** Cat, tell me, what other possibilities do the new driver from S3TurboTool have?

***Answer:*** You can reduce the voltage on the processor without using unlock, do not follow the steps 1-9 instructions and at the stage of the driver assembly, remove the "Unlock turbo" checkout. There is also the option "Bag SVID/FIVR," this will distort the display of real consumption of the processor, and therefore the AVX load will cease to fall the frequency, but accordingly, consumption will increase. Recommended for models that have a low factory TDP, for example the E5-2630Lv3.

----
*** Question:*** How to support?

***Answer:***

ser8989 - 5366-7280-9045-9598 (MTS Bank)

S.T.A.L.K.E.R - 5469-6700-1549-2427 (Sberbank)

Vasily Pupkin - 5368-2902-1226-6714 (VTB)

Snooki Lowe - 4817-7602-3407-9170 (Sberbank)

Koshak - 4276-6900-1026-7273 (Sberbank)

KOT JIETA - 5228-6005-4997-9898 (Sberbank)

Kostyan - 4276-0200-1999-5122 (Sberbank)

Thank you very much for your help!

----

About the post codes

Remember that in any problem, you should look at the socket for damage and clear the contacts of the processor, if you personally did not and are not sure about it. Also try to reset the settings of the biosap with a jumper.

Known solutions for certain post-codes:

* FF - anything; if the system is just assembled, then it is worth checking the socket for damage and clear the contacts of the processor; if the system has worked before, and the reset of the biosweeper does not help, it is worth flashing the bios; if the system after launch immediately turns off, having managed to show only FF, then it means that the system can not start the AP, or the BP immediately goes in defense for some reason
* 19 - occurs when trying to overclock overclock the processor models on the inappropriate biosay for this purpose; in other cases, it is worth flashing bios
* CD - installed V4 ES (they are incompatible)
DC - installed two different processors in a two-crepean system
* D6 - problem with the video card
* B2 - problem with the initialization of the video card
* AE - waiting for a bootable disk (if a black screen, then the problem in the video output mode)
* 53 - RAM not installed
* B7, BF - a problem with RAM (try reset biosampling the settings with a jumper)
* B0 - RAM is installed in the wrong slot (the slot filling sequence is broken)
* 92 - the system starts in the UEFI video mode, but this mode with the video card is not supported (try to reset the bioswing settings)

![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/.git_git_ix/ages06.png)
![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/git_git_ages/screen07.png)
![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/._gitimages/08.png)

If you observe the frequency of the system bus is less than 99.75MHz
For example, 98MHz. In this case, you will not get 100MHz, even if you sew the appropriate bios. As far as we know at this time, the frequency underestimates the active Hyper-V in the OS.

*(thank you ***Vasilya Pupkin***)*

Also helps to disable the component "Windows Sandbox"

*(thanks ***C0oo1D***)*

Setting up the speed control of fans for Huananzhi X99-8M/8MD / F8/T8/TF

It is a customizable curve of revolution dependence on the temperature of the processor. The five points of this curve are adjusted. T1 determines the temperature before reaching which the revolutions defined in PWM1 (value in %) will be reached. The T5 determines the temperature, after which it will be 100% revolution. T2/T3/T4 are intermediate points by which it is possible to construct a curve between T1 and T5.

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/git_gitages/screen04.png)

On the chart above, a variant of the kot-versions of the bios. Up to 45 degrees, the minimum revolutions (30%) are supported and then linearly grow to 100% at a peak of 80 degrees.

For better understanding, consider another option.

![](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/.gitimages/screen05.png)

What is a Tbase0? This is a customizable shift of the exposed temperature values. At a value of 0, the temperature values coincide with the temperature of the CPU Package (DTS). There is no Tbase0 setting in the biosp. in the 2020-17 version, but this offset has a value of 15, which is why all the temperature values in the setting are underestimated by 15 to match the desired.

Also, the bios from 2020-08-17 allows you to configure the % of the revolutions of the 4pin-fventilator connected to the CPU_FAN2 connector (X99-T8/TF). The speed is static and will not depend on the temperature. Setting within 0-255 values.
* 0% - 0
* 10% - 25
* 20% - 51
* 30% - 76
* 40% - 102
* 50% - 127
* 60% - 153
* 70% - 178
* 80% - 204
* 90% - 229
* 100% - 255

This mode is also supported for CPU_FAN1. It is convenient to explore the possibilities of your fan before adjusting it.

There is also a problem that disrupts the work of speed management after the system exits the sleep regimen. CPU_FAN1 accelerations are fixed at 50%, and CPU_FAN2 (X99-T8/TF) revolutions are fixed at 100%. The program [Ultimate Patcher Tool]] (Ultimate-Patcher-Tool) has a fix of this problem for the 2020-05-25 bios.

If you have a socket damaged

It is neat to correct the legs of the socket, for example, with a toothpick or similar object.

![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/w/master/.git_gitimages/09.png)

![]https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/raw/master/.git_mits/screen10.png)

The images above marked the legs, the absence of two or three of which is uncritical, because. The legs are duplicated many times. If you have irreversibly damaged other legs, there may also be a chance for the successful operation of the system, for this you need to check with the texting or write to [Telegram group](https://t.me/russian_xeon_community).
