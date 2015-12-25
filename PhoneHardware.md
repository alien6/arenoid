# Phone Hardware/Drivers #

Please look for datasheets and drivers (e.g. in other Android phones)and paste the links in comments.
| **Chip** | **Type** | **Description** | **Driver** |
|:---------|:---------|:----------------|:-----------|
| [PMB8878](http://www.infineon.com/cms/en/product/PSLPopup.html?productType=db3a3043156fd573011594a557d60747) | BaseBand | S-GOLD3H Baseband Processor system - baseband IC combined with a 3G coprocessor IC, running with Nucleus RTOS: ARM926EJ-S, the Main-CPU (Processing core) & ARM7 TDMI-S, 3G Coprocessor Subsystem | [Yes, we can get the drivers from iDroid - Android on iPhone](http://www.idroidproject.org/wiki/Status) |
|AMD IMAGEON A250 | Application Processors |ARM1176JZ-S Processor combined with 2D/VG Graphics, Imaging, Display, Video, Audio and Security engine | NO         |
| PMB6821  | Controller | the Power-Management controller | NO         |
| PMB6952  | Controller | PMB 6952 SMARTi 3GE combined SMARTiPM quad-band GSM/EDGE and SMARTi3G triple-band WCDMA transceivers in a laminate based PG-TFSGA-121-2 package | NO         |
| WM8990   | Multimedia Controller | the multimedia chip |1.) [Yes, included in the Andorid SRC](http://android.git.kernel.org/?p=kernel/common.git;a=commitdiff;h=97bb8129e5deb3c0584391a5d2348966732e2233) 2.)[Another Link](http://www.spinics.net/lists/alsa-devel/msg23195.html) |
| Flash #1 | ROM      | 8Gbyte eSD Version 2.1 : SD I/F (I-NAND), Storage of the User-files & LG propritary OS| NO         |
| Flash #2 | ROM+RAM  | 2G NAND + 1G DDR SDRAM | NO         |
| Camera   | Cam      | 5 Mega pixel Camera, Micron MIPI | NO         |
| TCM9000MD | VT Cam   | 2Mp FrontCam    |
| Hitachi IPS | Display  | 2.98", 480x800 WVGA, 16.777.216 True color TFT | NO         |
| T1007A   | Touchscreen Controller | Synaptics ClearPad 2000 - Capacity touch sensor driver  | [Yes, Google NexusOne got the same Chip](http://www.geek.com/articles/mobile/nexus-one-teardown-thoughtful-design-top-notch-engineering-2010017/) |
| BD6088GUL | Backlight | Intelligent LED Driver - 6 white LEDs in parallel connection | NO         |
| BCM4325  | Radio Controller | Low-Power 802.11a/b/g with Bluetooth® 2.1 + EDR and FM | [Yes, included in Android SRC](http://android.git.kernel.org/?p=platform/system/wlan/broadcom.git) |
| [MAX9722BETE](http://www.digchip.com/data/280/280-1978-MAX9722A.pdf) | Audio Controller | Audio amplifier | NO         |
| TQM7M5005 | GSM Controller | GSM Power Amplifier Module | NO         |
| ?        | ?        | Micro SD Memory Module with eight exposed contacts on one side | NO         |