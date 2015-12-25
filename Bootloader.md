# Bootloader #
As fare as we are now, we know a couple of things about the different bootloaders.

The build in bootloaders are at least two the EBL (Emergency Bootloader) and the AMD\_BL1 (S-Class Bootloader).


![http://img299.imageshack.us/img299/4417/bootuparena.png](http://img299.imageshack.us/img299/4417/bootuparena.png)


By pressing the Power Button, the bootrom of both processors initializes each bootloader:
  * The bootrom of the BaseBand (S-Gold Chip) initializes the EBL.
  * The bootrom of the AMD Imageon 250/9 initializes the AMD\_BL1.

The bootloaders initialize each of their kernel:
  * The EBL loads up the BaseBand Kernel (BB\_MPEH).
  * The AMD\_BL1 loads up the AMD Kernel (a250img.bin included in AMD\_BL2 partition).

The kernel got their own software partition:
  * The BaseBand Kernel got the BB\_CUST / ROOT partition.
  * The AMD Kernel got the AMD\_OEM Partition (includes VUI files for S-Class modding).