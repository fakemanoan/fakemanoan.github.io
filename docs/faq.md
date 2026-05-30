---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## My device isn't supported!
Some use different modems, NFC chips or different components. This would require a separate install package.  

Some are completely different devices. I would need access to a device for several days debugging.

Given technical/time limitations (and for simplicity), it is not possible for me to support everything.

If you would like to help me add support, open a pull request on [GitHub](https://github.com/samsungexynos7420) with the necessary changes.

## What Gapps should I use?
Use MindTheGapps_Legacy (ARM64), a package I created to make MindTheGapps work on our TWRP. It is all explained [here](../downloads/mindthegapps)

Other Gapps packages are not supported. YMMV.

## My SIM card isn't detected! I can't enter my SIM unlock code!
A quirk with S6 and S6 edge devices prevents you from entering your SIM unlock code. You must remove it on the Stock Sasmung ROM or on another phone.

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
Some Samsung devices struggle with their proprietary noise cancellation on LineageOS.

The problem can be mitigated somewhat with mixer_paths.xml tweaks, which I have done to the best of my ability. 

## I rebooted to recovery, and my TWRP is gone and replaced with LineageOS recovery!
You have selected "Update recovery" in the OTA updater.

You can turn this off by going to Settings -> System -> Updater -> 3 dots -> Preferences
And deselecting "Update recovery". You can then flash TWRP again. 

## When I download an OTA update, it reboots to recovery and does nothing!
Older TWRP recoveries do not support OTA updates, so will fail silently when updating. Currently, only my updated TWRP supports OTAs properly.

You can download my TWRP version [here](../downloads/twrp)

## My Camera doesn't sync the flash properly
The stock camera doesn't work well with our device. I suggest using GCam Go or Open Camera. 

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is a hardware issue, not an issue with the ROM.

## VoLTE/WiFi Calling isn't working!
All Samsung devices use a proprietary IMS stack, which is what is used for VoLTE and WiFi calling. This cannot work on LineageOS at this time.

If you require VoLTE and WiFi Calling I suggest using a stock ROM or a Samsung based ROM, like FloydROM or other OneUI ports.

## My touch is inverted after installing!
You installed the wrong file. Installing an S6 edge file on an S6 (and vice versa) will cause this behavior

The way to fix it is to install a stock ROM, and reflash the touch firmware. 

Once you are in stock firmware, open the phone dialer. Type * #2663# *. Then tap TSP update. This should fix your problem. 

## When is the next release?
No idea. But generally asking for an ETA is a bit frowned upon ("are we there yet?")

## Can you build Android 15, 16, 17 etc?
If I do, you will see it! Newer versions of Android demand newer kernel features, which need to be backported. In some cases this is not practical. 

## Can you build [other ROM name here]?
Maybe.  

I build LineageOS due to their consistent stability and security patches. I could mass produce 1 off builds of [insertname]OS. Many of these OS projects copy things from one another until they are essentially the same thing anyway. But one day, I may build a customization or privacy focused ROM. 

You can build that ROM yourself if you like. All source code is on github! 

## Sometimes my phone turns black and when I turn it on, it's just a black screen with a clock!
Your hall sensor is likely broken. Samsung devices have 2 magnets for flip cover detection 1 in the bottom left and one in the top right, which I have support for in my ROM. This is likely a hardware issue.

You can disable this in settings -> Connected devices -> connection preferences -> smart cover. 

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.