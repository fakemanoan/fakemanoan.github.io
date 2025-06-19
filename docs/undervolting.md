---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Undervolting (and Overclocking)"
---
[ <-- Back](../)

## What is undervolting?
Every piece of silicon requires power to run. A certain amount of voltage is required to reach a certain clock speed. The higher the frequency, the more voltage is required, and vice versa. This is no exception for our Exynos 7420 SoC. 

In more recent years, enthusiasts have turned to undervolting to get more performance. This is useful when we are power or thermally constrained (with the Exynos 7420 we are with both).

We run on an early 14nm node from Samsung, which is notorious for running hotter and not hitting high clocks. The next generation of 14nm from Samsung was much better, but sadly we dont have access to such a chip.

Adding some kernel patches, we can alter the DVFS tables for the CPU and GPU to reduce voltatages yet keep the same performance.

We simply cannot just lower the voltages, as it may not be stable at lower voltages, resulting in crashing or instability in apps. We must run a stress test to ensure we are stable. Try running Geekbench, PCMark or 3DMark on a loop to find instability (hard lock up or crash)

If you do this correctly, you can increase performance and potentially increase battery life. 

You can approximate how good your SoC is based on the ASV values that are reported by the kernel. You can find this value in hKtweaks under 'device'.

Higher ASV values indicate more undervolting capability. There are ASV values for big and little cores, memory bus, GPU and the ISP.  

Start with -25mV and gradually decrease voltage until it is unstable. 