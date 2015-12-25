# Introduction #

This page describes how to use the Flashtool. With this tool you can upload and download partitions from your computer to your mobile phone.

# Step 1 - Setting up Drivers and the Flashtool\_E2 #

You can download a zip file with useful files in it <a href='http://www.file-upload.net/download-2690460/Fullbackup-Km900.zip.html'>here</a>.
This zip file contains everything needed for up- and downloading partitions even if you haven't used the flashtool before.

Now, in order to run the Flashtool needs some prerequisites:
  * The LG Modem driver
  * 01\_psi\_large\_block\_16\_bit\_paging.flb (for downloading and adresses)
  * 06\_BB\_MPEH.fls (for uploading)
  * the Flashtool itself (if not already downloaded)
  * some preferences

Unpack the "LGUSBModemDriver\_WHQL\_ML\_Ver\_4.9.5\_All.zip" and install the "LGUSBModemDriver\_WHQL\_ML\_Ver\_4.9.5\_All.exe". If you have upgraded you phone software recently you may skipt this driver installation because it's already installed.

You may folow <a href='http://code.google.com/p/arenoid/wiki/KDZExtractPack'>this guide</a> on how to extract a kdz file to get the "01\_psi\_large\_block\_16\_bit\_paging.flb" and the "06\_BB\_MPEH.fls" from any kdz file. It is highly probable that you can use these files from any kdz file even if the versions of the Firmware in the kdz and on your phone differ. However, if you want to be _death proof_ - use those two files from the kdz which has the same version than your phone has.

Now you have the Flashtool and the files? Then you only need to have the following preferences selected in your Flashtool. (If you downloaded the Flashtool from the link above then this is not neccessary):
Go "File" - "Settings". In "Setup" check "Enable Binary Mode" and in "Auto Start" check "Auto Start (DSR / USB detection).

Now we can upload the first partition.

Oh hold on: We have one last step to do:
  * shut down your phone
  * _release the battery_
  * plug your USB cable into the phone
  * **do not!!!** plug the other end of the cable into the computer (we'll do that later)

# Step 2 - Copy Basics #

Copying partitions can be compared to copying files from a giant USB stick. The big difference is that on a flashdrive the flash controller selects where to put the bits and bytes. On your phone every partition has a predefined adress where it should be. Any partition also has a certain length. So to read or write a partition you tell the Flashtool **where** to start and **how long** to read / write from there.

Another thing most people have trouble becoming friends with is the Up- and Downloading names:
**Up\*loading means _from your phone to your computer_.**Down\*loading means _from your computer to your phone_.
You can remember that easily if you just know that here we think from the _phone's point of view_. Your phone has to upload data to the computer and recieves (downloads) data from there.

Ready for taking action? Then let's start.

# Step 2 - Uploading #

The safer thing to do is copying a partition from your phone to your computer. Even if the process fails your phone should still function normally.
For Uploading select "Binary" - "NAND" - "Upload".

In "Destination" choose a bin file to download the partition into.

In "EBL Reference" the "06\_BB\_MPEH.fls" from your kdz should be selected.

Now we only need the "Adress" and "Length" of the partition you want to upload. You can find the adresses of the firmware parts <a href='http://code.google.com/p/arenoid/wiki/MemoryMap'>here</a>.
These adresses are written in the 01\_psi...fls file - but in there they are kind of reversed. If you are interested in how to read them there, check **this out**.

---

Communication Setup usually doesn't need to be changed. We need a BaudRate of "921600", a channel of "1" and the "Infineon USB Driver" as the communication driver.

With all this selcted you can click start. Still don't plug your USB cable into the computer. The Flashtool warns you that COM1 wouldn't be writable. Just click "Yes".

Now a window named "Download" appears (even if we upload, so don't panick). **This is the time** to plug your phone into the computer. The Flashtool will realize your phone being plugged in and immediatly start uploading.

You should see your bootscreen for a split second on your phone's display followed by blackness (on the phone). In the "Download"-Screen you should see the process.
You can read about the device being synchronized and you can see the percentages of the progress passing by.

**_IF YOUR PROGRESS STARTS BUT TIMES OUT AT 82% OR SO --> NO PROBLEM!_** read below

# Step 3 - Some strange things about length #

Usually you can access the phones partition with the lengthes and the adresses of the 01\_psi...flb. However, sometimes these values are wrong!

If they are wrong (which they are at least at the partitions _Root, AMD\_OEM and AMD\_OEM\_Data_) the Upload is cancelled at a certain level of percentage.

If you stumble across a cancelled Upload: Don't mind. Try opening the bin file with WinImage. If you can do so the upload was correct (but the length was wrong).

If you encounter such a case you have to download the file with a different length but we'll see that in the next step.

# Step 4 - Downloading #

You still have to have "Binary" selected in the Flashtool but we work with "NOR" and "Download" instead. Next to the radiobuttons "NOR" and "NAND" you can find a link to a "Project File". Select "Use external file" from the dropdown menu and select your "01\_psi\_large\_block\_16\_bit\_paging.flb".

Further down select your bin file.

Now enter the adress and length accordingly. Do not use "Auto" (it at least didn't work for me) and leave the file offset at 0x00000000. The Communication Setup stays the same as it was while Uploading.

If you had a cancelled upload but can edit the bin file you have to recalculate the download length (read below).

You can then do the same steps as before:
  * click on "Start"
  * click on "Yes"
  * plug in your (battery less) phone
  * wait for the downloading process to finish

**Recalculation of the download length**
If the partition upload was cancelled but you where able to edit the bin file with winimage you have to recalculate the size of the bin file. Copy the length to the clipboard (**not** the length on the harddrive which may be too long).
This is easy. Rightclick on your bin file and bring up your file properties. You will be given two lengthes.
Paste the correct length (number of bytes) into <a href='http://de.selfhtml.org/helferlein/dezhex.htm'>this</a> tool. Delete the points (or commas) which windows uses to seperate every 3rd digit block and press "dez->hex".

You will be given the correct length of this partition. _Down\_load this partition with this length._


Now you are able to upload and download partitions from (and back to) your phone. This is much easier than packing a kdz file all over again every time you change anything.