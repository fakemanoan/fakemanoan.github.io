---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## What Gapps should I use?
TLDR: ARM64 for the specific Android version

If you want to stick to LineageOS suggestions, MindTheGapps won't work on our device. However, I have created "MindTheGapps Legacy", which will work fine. It is a simple mod, and you can download or create your own by following this link [here](../downloads/mindthegapps)

Other Gapps, like NikGapps and BiTGapps, do not require modification and work as is. 

## I have echo in phone calls!
Samsung devices have echoing issues in LineageOS because noise cancellation does not work properly on Lineage. 

The problem can be reduced with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## My banking/other apps aren't working!
This is likely from your device failing attestation.

Play Integrity can fail for many reasons, like rooting, SELinux permissive, using common build fingerprints and lots of other things. Many apps will refuse to launch if you don't meet a certain level of integrity. You can check this using YASNC in the Play Store.

Other things, like custom ROMs (Lineage, crDroid), unlocked bootloaders, root access can prevent apps from working too.

There are ways around this, but it is constantly changing. Check XDA forums for updated advice about passing Play Integrity and other app specific issues.

## When I download an OTA update, it reboots to recovery and does nothing!
Older TWRP recoveries do not support OTA updates, so will fail silently when updating. Currently, only my updated TWRP supports OTAs properly.

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera doesn't work well with our device. I suggest using GCam Go or Open Camera. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
Samsung uses proprietary IMS, which cannot be easily integrated or reversed into AOSP based ROMs (like Lineage). This affects all Samsung devices, not just the S6/Note 5.

If you need VoLTE or VoWiFi, you must use a Samsung based ROM, like FloydROM, A8 port, Ultimate Oreo or even Stock firmware. There are efforts by people to get these functions working in AOSP, but they are currently in testing and not stable for everyday use.

## When is the next release?
New builds will be released when they are ready. Asking for a new build doesn't make one appear. 

## I can't enter my SIM unlock code / my network isn't working!
Currently there is a bug relating to LTE networks and SIM unlock codes on the S6 and S6 Edge. 

I would suggest removing the SIM unlock code prior to flashing the ROM, or removing it on another phone.

Sorry for any inconvenience, but it is better than having broken call audio.

## Can you add X, Y, Z to your builds?
If it is a reasonable request may be.

## Can you build Android 14, 15, 16, etc?
Probably not.

There are certain technical and logistical reasons as to why I won't build those versions. It won't happen currently.

Asking persistently for a release or ETA will not change my mind.

## Can you build [other ROM name here]?
If there are enough requests or I have an interest in it, yes. 

I am not a fan of building 20 ROMs. Each one should have a purpose for existing. Currently, I am for long term stability and security, so the ROMs I build will reflect that.

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.