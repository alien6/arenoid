# FlashtoolE2 - Hex Adresses #

1. Shut down the phone and remove the accu and remove the cable

2.Open [Flashtool E2](http://www.multiupload.com/UVHWY534ZI) (use the Flashtool\_E2\FlashTool\_E2\Flashtool\_E2.exe)

3. Click Binary Mode (not "Normal")

4. FLASH Type "NOR", Project (Hardware Setup) Use [External File](http://www.multiupload.com/P0ET7YU18S)

5. Click on "Upload" (Load it from the phone to your PC.) or "Download" (Load it from your PC to the phone)

6. Example: If you want to download/upload the AMD\_BL2 partition (it includes the a250image.bin), write in "Binary File" C:\amd\_bl2.bin

7. [Check the start adress and length](http://code.google.com/p/arenoid/wiki/MemoryMap) of the prefered partition and write them in the fields. When uploading you'll have to do the same and set the rest like this: "Auto" == OFF, File Offset 0x00000000

8. In Communication Setup choose Channel "1" and Communication Driver "Infineon USB Driver"

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/hex.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/hex.jpg)

9. Press start (if necessary click on "yes", too)

10. Plug in the cable (your phone WITHOUT battery) and your download/upload should start.
Sometimes it can take a while...

11. Open the partition with [WinImage](http://www.chip.de/downloads/WinImage_12994161.html)  -> (some partitions aren't partitions, like EBL and AMB\_BL1 (bootloaders))