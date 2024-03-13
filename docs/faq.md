---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## What Gapps should I use?
Our devices need ARM64 Gapps, so make sure you download that type for whatever Android version you use. 

If you want to stick to LineageOS suggestions, MindTheGapps won't work on our device. However, I have created something im dubbing "MindTheGapps Legacy", which will work. It is a simple mod, and you can download or create your own by following this link [here](../downloads/mindthegapps)

Other Gapps, like NikGapps and BiTGapps, do not require modification and work as is. 

## I have echo in phone calls!
Samsung devices have echoing issues in LineageOS because the noise cancellation does not work properly on Lineage currently. 

The problem can be reduced with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## My banking/other apps aren't working!
Chances are this is due to your device failing attestation checks.

You need to pass SafetyNet/Play Integrity API in order to use "secure" apps, like banking for instance. Since our devices use SELinux Permissive, we can't pass these checks. However, with Magisk modules, you can bypass these checks easily.

Check XDA forums for updated advice about passing SafetyNet/Play Integrity.

## When I download an OTA update, it reboots to recovery and does nothing!
You need to use my updated TWRP recovery or it will not do anything. Previous recoveries built for our devices do not support OTA updates, so will just fail silently. 

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera app does not work well with our device. I would suggest using GCam Go or Open Camera. Others have noted success with the GrapheneOS Secure Camera too. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
Samsung uses a proprietary IMS implementation, which provides the ability to use VoLTE/VoWiFi, and this cannot work on LineageOS. 

For now, it is not possible to do this on any custom Android version. If you need these features, you will need to use a Samsung based ROM. 

## When is the next release?
The next release will come out when it is ready. I do this in my free time remember!

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.