# COPIED FROM MAD-ATV_dev
> [!CAUTION]
> Do NOT use 2K/4K/8K screens/monitors - it will not show anything after initial PoGoROM logo. Find older 1080p monitor, check if you can fake/downgrade resolution on yours 4K TV. If you can't and you have none you can still use [scrcpy](https://github.com/Genymobile/scrcpy "https://github.com/Genymobile/scrcpy") but as this is software it's funky/Android dependable.

> [!WARNING]
> Do not use Notepad, do not open those text/sh/cfg/ini files, do not copy-paste them to Wordpad, etc. 
> Windows encoding/lines bad. Right click on those .sh and select "Save as" or just open in new window in web browser and click CTRL + S.

One of my devices USB was not detecting thumbdrives. So instead of picking thins from USB I changed the screipts to look at sdcard. You need to push 01MAD.sh and mad_autoconfig.txt to /sdcard :

Get ADB working where you can push files to device.

Download [01MAD.sh](https://raw.githubusercontent.com/Yhatax/MAD-ATV_dev/main/01MAD.sh "01MAD.sh"). to c:\
adb push c:\01MAD.sh /sdcard

Download `mad_autoconf.txt` from MADMin -> System -> Auto-Config and c:\
adb push c:\mad_autoconf.txt /sdcard

Once they are copied, you'll need to give 01MAD.sh permisions to execute, I moved it to system/bin and chmod 775:
adb shell
su
chmod 775 /sdcard/01MAD.sh

Then execute 01MAD.sh
sh /sdcard/01MAD.sh

After finishing:
rm /sdcard/01MAD.sh
