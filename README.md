Hackintosh on HP Elitebook 840 G6
1. Hardware specs:
   - CPU: Whiskey Lake i5-8265u
   - Memory: 16 GB
   - Hard drive: WD Blue SN580 500 GB NVME m2 (partitioned into 2 equal partitions: one for Hackintosh, the other for Win 11)
   - Wireless: Intel Wi-Fi AX200
   - Graphic: Intel UHD 620
2. Hack info:
   - Opencore: 0.98
   - macOS: Sonoma 14.3
   - SMBios: MacBookPro15,2
3. Observations after hack:
   - Pretty much everything works with exception of the built in microphone, using the microphone jack doesn't help. The work-around is to use a bluetooth headset
   - iServices: works with physical ethernet connection, but not with wifi. This is due to the limitation of current AirportItlwm.kext (2.3.0 alpha). Hopefully, the official release will address this issue.


Notes for using this hack on your machine:
 - At the very least, your machine model should match that of mine: HP Elitebook 840 G6. It is specifically for Whiskey Lake, similar CPU family might work, but I don't have a way to test it!
 - You should ignore (i.e.: remove) my "USBMap.kext" and use "USBInjectAll.kext" for installation, then follow the post-installation guide to create your own "USBMap.kext". DO NOT use it for installation on your machine
 - I have the Real Time Clock (RTC) issue, which fixed by enabling the quirk [DisableRtcChecksum] to true
 - It has been upgraded to OC 0.99 and Sonoma 14.3.1 (Attempt to upgrade to Sonoma 14.4 failed!)


Credits: Thanks to the followings to make this happened
- Opencore: for Opencore of course
- Apple: for macOS
- Dortania: for the guide
- Referecing this repo https://github.com/yusufklncc/HP-EliteBook-840-G6-Hackintosh/tree/main for additional ACPI content to resolve the "card icon" issue!
