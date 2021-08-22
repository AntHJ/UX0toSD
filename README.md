# UX0-to-SD
This is possibly the easiest way to setup your SD2Vita, PSVSD or PSTV USB Drive.

![Screenshot](https://github.com/AntHJ/UX0toSD/blob/main/Vita.jpg)

Simply run the tool the 1st time and select which adaptor you are setting up.. the app will remove and previous attempts to setup your SD and then set the card as a secondary storage drive (grw0:) and reboot the system.. Once rebooted, just run the app a 2nd time to start the data transfer stage..

If for some reason you see an error detecting your card then the possible issues could be :
    
    1 - Fake or Faulty SD card. (this is most commonly the main issue)
    2 - You could have a faulty adaptor. (the SD2Vita adaptors are fragile)
    3 - The SD card wasn't properly zzBlanked or formatted. (also quite common)
      
After all the data has copied from your current UX0 (the Sony memory) to the card the app will then set your SD as the primary storage and set the Sony memory card (if applicable) as a secondary storage (uma0:). this is only really useful if you have a good size Sony card. you can remove the Sony card and put it safely away just in case its needed in the future.

Finally, after the system reboots again with the new allocations and newly copied SD you can go into Setting -> System -> System information, you should now see your SD cards memory size (Capacity) .. BE AWARE.! the size show is and should always be much smaller then the printed size (usually around 93%)

    Examples of good SD capacity :
            128gb   shows as between 116gb -> 119gb
            256gb   shows as around 238gb
            400gb   shows as around 372gb
            515gb   shows as around 476gb
            
    Note : any SD cards showing higher values than these are most likely fake
    
# Preparing the SD
You can either unlock My additional tool in the app if your card is not detected, or manually download my Tool [-here-](https://github.com/AntHJ/UX0toSD/blob/main/FormatTool-lite.zip)
otherwise there are other more recognised methods where basically you will flash a file named zzBlank.img using the Win32Diskimager software to the card then fornat it as exFat. if your SD is upto 128gb then format it with the file allocation as default but anything over 128gb NEEDS to be format at 64k or you card will waste space over time.

My Tool is the easiest option but either is fine.. the general reason for this is that the Vita needs to write data at the very begining of the card to recognise properly and needs to be in the correct storage format. the file allocation size is a little tricky to explain but basically 64k makes the wasted spaces smaller

    For cards upto 128gb, use exFat and (default) file allocation
    For cards over 128gb, use exFat at 64k file allocation
