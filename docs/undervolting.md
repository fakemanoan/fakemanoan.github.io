---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Undervolting (and Overclocking)"
---
[ <-- Back](../)

# What is undervolting?
Every CPU, SoC or active silicon circuit requires power to run. The higher the voltage, the higher the clock speed you can run. Manufacturers may intentionally overvolt CPUs for stability or binning purposes, leaving some voltage headroom.

In recent years, undervolting has became popular in _power_ or _thermally_ constrained devices in order to get more performance and battery life. Since our Exynos 7420 runs 🔥 **hot** 🔥 and is power hungry, this is perfect for us!

Adding some kernel patches allows the voltages of the CPU, GPU and various internal buses to be altered. This is an early 14nm Samsung foundry chip, so results may not be great compared to a later Exynos 8890 14nm, but any improvement is welcome.

## Some notes
- This requires a supported kernel
- Root access
- Stability tests are mandatory to ensure your data doesn't get corrupted

_**You cannot simply lower voltages**_ and go, as your device may crash after some time. You must run a stress testing app to ensure you don't crash randomly. Try running Geekbench, PCMark or 3DMark for some time to find glitches, abnormalties, crashes or reboots. If you find none, you are stable!

There is a marker for how good your chip is, an **"ASV summary"**, which can be accessed in hKtweaks under "Device" or by reading the sysfs value in a terminal emulator:

``
"/sys/kernel/debug/asv_summary"
``

### Example output
``
big:8, LITTLE:9, INT:9, MIF:9, G3D:7, ISP:9
``

Higher ASV values indicate more undervolting capability. Look for people with similar values and their undervolts. Remember: nothing is guaranteed!

If you do this correctly, you can increase performance and battery life while reducing thermals. It is worth it if you can tune it in. 

# Undervolting tools
I would suggect using my **updated version of hKtweaks V2.2.4**. 

## Download for hKtweaks v2.2.4
- [hKtweaks v2.2.4 GitHub Link](https://github.com/fakemanoan/hKtweaks/releases/download/v2.2.4/hKtweaks_v2.2.4.apk/)

It supports our Exynos 7420 SoC better compared to the previous V2.2.2.  

You can also do this via commands, but it is not fun that way

# General guide
- Start with -25mV on BIG and LITTLE cores and gradually decrease voltage until it is unstable, running tests at every change.
- Do the same for GPU and the buses.
- Post your results on XDA so that others can try out your settings.