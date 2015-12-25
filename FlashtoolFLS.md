# FLS Files #

These files can contain multiple partitions (bin files). Where the UpTestEx tools cope with kdz files, the Flashtool uses fls files for having many partitions packed together.

# Flashing them... #

Flashing fls files is easier than you might think. If you have already read <a href='http://code.google.com/p/arenoid/wiki/Flashtool'>this guide</a> then you're well prepared.
As described there, you have to get rid of the battery and plug the phone in the computer at the right time (**now** is not the right time).

Open your Flashtool and select the mode "Normal" (not "Binary").

In this screen you can only select your fls file.

Once opened, you see many details of the partitions in the file. If your Infineon Driver is still selected ("Communication Setup" at the bottom of the window) you can just click on "Start". After having clicked on "Yes" you can plug in your phone and wait for the flashing to finish.

You do not have to enter adresses or lengthes because they are alsready written in the fls file.

# But what is the purpose? #
Unfortunately we cannot create fls files (if you can, let us know and we'll work out a guide!).
There is an fls file which helps you "reanimating" your phone if it shows "version mismatch" <a href='http://www.megaupload.com/?d=2DFYO9KT'>here</a>.