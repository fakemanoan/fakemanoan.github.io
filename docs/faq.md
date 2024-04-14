---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## What Gapps should I use?
TLDR: ARM64 for the Android version downloaded

If you want to stick to LineageOS suggestions, MindTheGapps won't work on our device. However, I have created something im dubbing "MindTheGapps Legacy", which will work. It is a simple mod, and you can download or create your own by following this link [here](../downloads/mindthegapps)

Other Gapps, like NikGapps and BiTGapps, do not require modification and work as is. 

## I have echo in phone calls!
Samsung devices have echoing issues in LineageOS because the noise cancellation does not work properly on Lineage currently. 

The problem can be reduced with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## My banking/other apps aren't working!
This is likely from your device failing attestation.

You need to pass SafetyNet/Play Integrity API in order to use some apps. Since our devices use SELinux Permissive (and Google shenanigans), we can't pass these checks. However, with Magisk modules, you can bypass these checks easily.

Check XDA forums for updated advice about passing SafetyNet/Play Integrity.

## When I download an OTA update, it reboots to recovery and does nothing!
You need to use my updated TWRP recovery or it will not do anything. Previous recoveries built for our devices do not support OTA updates, so will just fail silently. 

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera doesn't work well with our device. I suggest using GCam Go or Open Camera. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
Samsung uses a proprietary IMS that is hard to get working in Lineage, so currently doesn't work

This may change in the future, but if you require VoLTE or WiFi calling, you should stay with Samsung based ROMs (ie Ultimate Nougat, Ultimate Oreo, NobleROM, FloydROM etc)

## When is the next release?
New builds will be released when they are ready. 

## I can't enter my SIM unlock code!
Currently there is a bug relating to LTE and SIM unlock codes. I would suggest removing the SIM unlock code by flashing an older build (you can find it on the downloads page), or removing it with another device, until a fix is found. Sorry for any inconvenience, but it is better than having broken call audio.

## Can you add X, Y, Z to your builds?
May be. 

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.