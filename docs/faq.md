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

Other Gapps, like NikGapps and BiTGapps, do not require modification and work as is. (but are not supported by LineageOS so YMMV)

## My SIM card isn't detected! I can't enter my SIM unlock code!
Currently there is a bug relating to LTE networks and SIM unlock codes on the S6 and S6 Edge. 

You should remove the SIM unlock PIN on another phone or a stock ROM prior to installing the ROMs.

Sorry for any inconvenience, but this is required to have working call audio.

## I have echo in phone calls!
Samsung devices have echoing issues in LineageOS because noise cancellation does not work properly on Lineage. 

The problem can be mitigated somewhat with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## My banking/other apps aren't working!
This is likely from your device failing attestation. (Play Integrity/SafetyNet)  

You can fail these checks due to (but not limited to) the following reasons:
- Having a custom ROM
- SELinux Permissive instead of Enforcing
- Root and other mods
- Builds signed with public keys

Currently, only my Lineage 18.1 will pass **basic** integrity. 

Some apps still won't work. Check XDA for the latest advice on Play Integrity bypasses, as it changes frequently.

## When I download an OTA update, it reboots to recovery and does nothing!
Older TWRP recoveries do not support OTA updates, so will fail silently when updating. Currently, only my updated TWRP supports OTAs properly.

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera doesn't work well with our device. I suggest using GCam Go or Open Camera. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
Samsung devices use a proprietary IMS. This cannot be easily ported into AOSP or LineageOS. There are efforts to try get something working, but it's in the early stages and is buggy. 

If you need VoLTE or WiFi calling, you must use a Samsung based ROM, like FloydROM, Ultimate Oreo or even stock firmware.

## My touch is inverted after installing!
You have installed the wrong file. If you install an S6 recovery or ROM on an S6 edge (and vice versa), you will experience this issue.

The way to fix it is to install a stock ROM, and reflash the touch firmware. 
Once you are in stock firmware, open the phone dialer. Type * #2336# *. Then tap TSP update. This should fix your problem. 

## When is the next release?
New builds will be released when they are ready. Asking for a new build doesn't make one appear. 

## Can you add X, Y, Z to your builds?
If it is a reasonable request may be.

## Can you build Android 14, 15, 16, etc?
Probably not.

There are certain technical and logistical reasons as to why I won't build those versions. It won't happen currently.

Asking persistently for a release or ETA will not change my mind.

## Can you build [other ROM name here]?
If there are enough requests or I have an interest in it, yes. 

I am not a fan of building 20 ROMs. Each one should have a purpose for existing. Currently, I am for long term stability and security, so the ROMs I build will reflect that. Persistently asking for a ROM is not going to make it appear. Sorry.

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.