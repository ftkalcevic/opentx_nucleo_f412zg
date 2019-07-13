# opentx_nucleo_f412zg

Hardware and link to the firmware for a port of opentx 2.2 to STM Nucleo F412ZG

The updated firmware is in my [opentx](/ftkalcevic/opentx/tree/F412ZG) repository, in the F412ZG branch.

I use visual studio 2017 with visualgdb.  I used the following options when setting up the firmware build...

```
cmake -G "MinGW Makefiles" ../code/ -DCMAKE_PREFIX_PATH=d:\Qt\5.7\msvc2015 -DPCB=STM32F412ZG -DHELI=YES -DGVARS=YES -DTRANSLATIONS=EN -DLUA=YES -DMIXERS_MONITOR=YES -DTIMERS=3 -DWATCHDOG_DISABLED=YES -DSOFTWARE_VOLUME=YES -DMULTIMODULE=YES -DDISABLE_COMPANION=YES
```

I haven't ported the companion.

Directories...
 - OpenTx_NucleoF412zg - Circuit Studio PCB files.  Gerber files in the output directories.
 - opentx - git submodule pointing to the opentx source
 - opentx_visualgdb - visualgdb project files
 - opentx/code/nucleo-F412ZG.stm32cubemx - STM32 Cube MX file for this project.  It is only for pin allocation, not code generation.

The hardware has...
- 15 analog inputs
- 24 switches (2 or 3 position)
- No trim switches - I'm not sure what to do with these
- Xlite style UI - 128x64 OLED display, 5-way joystick, enter, exit, power button.
- I2S audio
- multi protocol adaptor support

