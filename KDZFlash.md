# KDZ - Flashing wit UpTestEx #

Now that you have already packed your kdz file you may want to put it on your phone.

In order to do this, enable every field on the right side of UpTestEx with WindowsEnabler (if you have to do so) and select your kdz file.
The "Version" string will be automatically selected. In "Phone Model" enter "KM900" and in "Loop Test Count" enter "1".

Now all you have to do is clicking on "Start Upgrade" and wait for about 15-20 minutes.


# Warning #
The UpTestEx tool likes communicating with LG. You should use it without an internet connection. They even find out your IMEI through the tool and could avoid support if you needed it.

## 2nd Warning ##
After the normal amount of time the log says "finished all test" and your phone **is in the loading mode**.

If your phone stays black and/or the flashing took less time than usual - there might have been errors.

If so, the best thing that could have happened is: nothing.

The worst thing could be a "version mismatching" - which means you'd have to <a href='http://code.google.com/p/arenoid/wiki/Reanimation'>recover your phone</a>.

To avoid such things: Be very careful with your edited partitions. They **mustn't** be larger than the original partition. If you add bigger PNGs - delete unneeded stuff! If they are too large the kdz won't work.