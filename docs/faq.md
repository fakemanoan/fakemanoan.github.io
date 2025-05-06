---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## What Gapps should I use?
ARM64 for the specific Android version

The LineageOS suggested MindTheGapps won't work on TWRP, so you must use a modified installer I created called "MindTheGapps Legacy". It is a simple mod, and it is all explained [here](../downloads/mindthegapps)

Other Gapps, like NikGapps and BiTGapps, do not require modification and work as is. (but are not supported by LineageOS so YMMV)

## My SIM card isn't detected! I can't enter my SIM unlock code!
There is a quirk with S6 and S6 edge devices that prevents you from entering your SIM unlock code. You must remove it on the Stock Sasmung ROM or on another phone.

Sorry for the inconvienice but it is required to get working phone calls.

## My banking/Whatsapp/other apps aren't working!
This is likely from your device failing attestation. (Play Integrity/SafetyNet)  

This can happen due to (but not limited to):
- Having a custom ROM
- SELinux Permissive instead of Enforcing
- Root and other mods
- Builds signed with public keys
- Unlocked bootloader

Check XDA for the latest info on bypassing Play Integrity checks. This is Google's fault, not mine.

## I have echo in phone calls!
All Samsung devices struggle with their proprietary noise cancellation on LineageOS.

The problem can be mitigated somewhat with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## I rebooted to recovery, and my TWRP is gone and replace with LineageOS recovery!
You have selected "Update recovery" when setting up the device. 

You can turn this off by going to Settings -> System -> Updater -> 3 dots -> Preferences
And deselecting "Update recovery". You can then flash TWRP again.

## When I download an OTA update, it reboots to recovery and does nothing!
Older TWRP recoveries do not support OTA updates, so will fail silently when updating. Currently, only my updated TWRP supports OTAs properly.

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera doesn't work well with our device. I suggest using GCam Go or Open Camera. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
All Samsung devices use a proprietary IMS stack which is what is used for VoLTE and WiFi calling. This cannot work on LineageOS at this time.

If you require VoLTE and WiFi Calling I suggest using a stock ROM or a Samsung based ROM, like FloydROM or other OneUI ports.

## My touch is inverted after installing!
You installed the wrong file. Installing an S6 edge file on an S6 (and vice versa) will cause this behavior

The way to fix it is to install a stock ROM, and reflash the touch firmware. 
Once you are in stock firmware, open the phone dialer. Type * #2336# *. Then tap TSP update. This should fix your problem. 

## When is the next release?
Builds are released when they are ready. I'm not sure when some builds will be done. Be patient and don't ask for ETAs.

## Can you build Android 14, 15, 16, etc?
In short, no. While technically it *is* possible, it will take time for me to update the kernel and other components to get appropriate support.

## Can you build [other ROM name here]?
If it is reasonable and attainable, may be.

I focus on LineageOS, as they provide consistent updates and most people use it. I am aware that LineageOS lacks some basic customisation features (I hate it too), but most people want LineageOS, and I have a finite amount of time. In the future I may build a PixelOS or crDroid for example, who knows. 

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.