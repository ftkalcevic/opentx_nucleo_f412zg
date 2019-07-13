# opentx_nucleo_f412zg

Hardware and link to the firmware for a port of opentx 2.2 to STM Nucleo F412ZG

The updated firmware is in my [opentx](/ftkalcevic/opentx/tree/F412ZG) repository, in the F412ZG branch.

I use visual studio 2017 with visualgdb.  I used the following options when setting up the firmware build...

```
cmake -G "MinGW Makefiles" ../code/ -DCMAKE_PREFIX_PATH=d:\Qt\5.7\msvc2015 -DPCB=STM32F412ZG -DHELI=YES -DGVARS=YES -DTRANSLATIONS=EN -DLUA=YES -DMIXERS_MONITOR=YES -DTIMERS=3 -DWATCHDOG_DISABLED=YES -DSOFTWARE_VOLUME=YES -DMULTIMODULE=YES -DDISABLE_COMPANION=YES
```

I haven't ported the companion.

Directories...

The hardware has...

n analog inputs
n switches

