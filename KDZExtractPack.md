# KDZ - Extract and Merge #
# Step 1: Merging Programs #

You'll need two programs: [LG UpTestEx Mod](http://www.multiupload.com/LIR8SFZ5Y5) and [WindowsEnabler](http://www.multiupload.com/FQIRO286RN)

Run both programs and click on the Windows Enabler Button (Taskbar) and make sure it says "ON"

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/weon.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/weon.jpg)


Go on UptestEx and click on all grey surfaces.

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestaktiv.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestaktiv.jpg)

# Step 2: Extract A KDZ #


Now click on "Tool" (upper left area) and then "Decrypt Kdz file".
A new window will open (you will have to click on the grey surfaces again!)

Select your KDZ and the result directory.

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestdec.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestdec.jpg)

Click on "Decrypt kdz File" and wait until it's done

Now start LG Utils [I'd recommend to put this tool in the same folder, your kdz has been extracted. - it will be easier.] in order to extract the files of the WDB.

When started, press "H", the WDB path (V10 _X_.wdb e.g. V10P.wdb) and the exact Firmware name (e.g. V10P\_00 or V10H\_00 or V10A\_01). Now wait a few seconds. Your extracted files are now on C:\ (I use Windows 7) so put them in the same folder as the WDB file. You can close LG Utils now.

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/wdbutils.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/wdbutils.jpg)

_**Step 2.1: Modding**_

_Now you can mod the "07\_BB\_CUST.dfat", "09\_a250\_image.fls" and "10\_a250\_oem\_code.fls" using Serj's FDIW.exe (http://www.multiupload.com/24QANVHPGU) and WinImage (http://www.chip.de/downloads/WinImage_12994161.html)_

# Step 3: UptestEx Configuration #


"Select Type" -> INFINEON

"Work Directory" -> the UpTestEx path

"Version" -> the version number you want to have

"Select model.dll" -> chose the Inf\_WebDnlf.dll

# Step 4: Create The New KDZ #

You'll need the extracted WDB files (which used to be on C:\):

```
01_psi_large_block_16_bit_paging.flb
02_slb_large_block_16_bit_paging.flb
03_ua_large_block_16_bit_paging.flb
04_BB_MPEH.dsp
05_BB_MPEH.eep
06_BB_MPEH.fls
07_BB_CUST.dfat
08_a250_bl1.fls
09_a250_image.fls
10_a250_oem_code.fls

\dll\IFWD_DownloadDll.dll
Inf_WebDnld.dll
Name.txt
mergeResult.txt
```

Click on "Add" in "Merge files" (left side) and add these files:

```
01_psi_large_block_16_bit_paging.flb
02_slb_large_block_16_bit_paging.flb
03_ua_large_block_16_bit_paging.flb
04_BB_MPEH.dsp
05_BB_MPEH.eep
06_BB_MPEH.fls
07_BB_CUST.dfat
08_a250_bl1.fls
09_a250_image.fls
10_a250_oem_code.fls
```

Click on the small arrow on/next to the "Add" button and choose "Add Text file.."

```
Name.txt
```

Click on the arrow again and choose "Add SUB Directory.." and add the extracted "dll" folder.

It should look like this:

![http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestdaten.jpg](http://i604.photobucket.com/albums/tt128/ahihad/Arenoid/uptestdaten.jpg)

<font color='red'>
<b>Warning:</b><br></br>
If you get this message: "merge_temp" doesn't exist,<br></br>
create the folder "merge_temp", create a TXT file (in merge_temp) and open it.<br></br>
</font>

Finally, press "Merge" and wait for about 2 minutes. Your KDZ file will be generated!


If you consider flashing the kdz file - be aware that the UpTestEx tools sends your IMEI number to LG servers. It is highly recommended to disable your internet connection while flashing. Mor info on flashing is <a href='http://code.google.com/p/arenoid/wiki/KDZFlash'>here</a>.

# Credits #

Thoughts and most pictures by okNNN

Translation, WDB part a bit more detailed and a short modding info (2.1)  by .:Crack:.