---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "FAQ"
---
[ <-- Back](../)
# FAQ
## I have echo in phone calls!
Samsung devices have echoing issues in LineageOS. The problem can be mitigated with mixer_paths.xml tweaks, which I have done to the best of my ability.

## What Gapps should I use?
If you want to stick to LineageOS suggestions, MindTheGapps won't work on our device. However, I have created something im dubbing "MindTheGapps Legacy", which will work. It is a simple mod, and you can download or create your own by following this link [here](../downloads/mindthegapps)

Other gapps, like NikGapps and BiTGapps, do not require modification and work as is

## My banking/other apps aren't working!
Chances are this is due to your device failing attestation checks.

Certain apps need your device to pass Play Integrity API. This is a test to see whether or not your device can be trusted. Currently, our device is not trustworthy due to SELinux Permissive, among other issues. In the meantime, you can install Play Integrity bypass modules in Magisk to get around this limitation mostly. Refer to general XDA threads for these issues.

## My phone shuts off randomly and when I plug it in, it is at 0%!
Your battery is severely degraded and needs replacing. This is not an issue with the ROM.

## When is the next release?
The next release will come out when it is ready. I do this in my free time remember!

## I am experiencing an issue not on this list!
Head over to [reporting a bug](../bugreport) and follow the instructions.