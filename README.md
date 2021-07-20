# UX0-to-SD
This is possibly the easiest way to setup your SD2Vita, PSVSD or PSTV USB Drive.

![Screenshot](https://github.com/AntHJ/UX0toSD/blob/main/Vita.jpg)

Simply run the tool the 1st time and it will set the SD as a secondary storage drive and reboot the system.

    Note : if your using a PSVSD or USB drive then hold the R trigger  while pressing X to start )

Once rebooted, run the app a 2nd time to start the data transfer stage.

    Possible reaons for an undetected SD / GRW0 :
      1 - Fake or Faulty SD cards are usually the main issue
      2 - You could have a faulty adaptor, the SD2Vita adaptors are fragile
      3 - The SD card wasn't properly zzBlanked or formatted
      
After all the data has copied from your UX0 to the SD card you will be asked if you want to use the Sony memory card slot as a secondary storage option. If you choose NO, the card will not be assigned and will be safely hidden. choosing YES will make the card visible as the partition UMA0. this is only really useful if you have a good size Sony card.

Finally, after the system reboots again with the new allocations and newly copied SD you can go into Setting - System information, you should now see your SD cards memory size.. be aware that the size show is and should be, smaller then the printed size (usually 93%)

    Examples of good SD capacity :
            128gb   shows as between 116gb -> 119gb
            256gb   shows as aroud 238gb
            400gb   shows as around 372gb
            515gb   shows as around 476gb
            
    Note : any SD cards showing higher values than these are most likely fake
    
# Preparing the SD
You can either unlock My additional tool in the app if your card is not detected, or manually download my Tool [-here-](https://github.com/AntHJ/UX0toSD/blob/main/FormatTool.zip)
otherwise there are other more recognised methods where basically you will flash a file named zzBlank.img using the Win32Diskimager software to the card then fornat it as exFat. if your SD is upto 128gb then format it with the file allocation as default but anything over 128gb NEEDS to be format at 64k or you card will waste space over time.

My Tool is the easiest option but either is fine.. the general reason for this is that the Vita needs to write data at the very begining of the card to recognise properly and needs to be in the correct storage format. the file allocation size is a little tricky to explain but basically 64k makes the wasted spaces smaller

    For cards upto 128gb, use exFat and (default) file allocation
    For cards over 128gb, use exFat at 64k file allocation


** For a quick video of this all in action, goto  **
https://youtu.be/h1Z_QXqHtKw
