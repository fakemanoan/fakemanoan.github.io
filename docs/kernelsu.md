---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "KernelSU"
---
[ <-- Back](../)
# Kernel SU support for Exynos 7420
Kernel SU is a kernel root soultion. This is different from Magisk you install via a ZIP.

KernelSU can be harder for apps to detect, meaning you have a greater chance of passing Integrity and root checks.

You cannot use Magisk and KernelSU together.

This is possible due to GitHub user @backslashxx porting KernelSU to legacy kernels.

# How to use KernelSU
Because this is an unofficial port, we cannot just use the regular KernelSU manager. You will have to download backslashxx's modified manager instead. This can be found here:

[https://github.com/backslashxx/KernelSU/releases](https://github.com/backslashxx/KernelSU/releases)

After you have installed that, you can use KernelSU as normal. 

Kernel SU is only supported on Lineage 18.1 at this time. It will come to later versions.

SusFS is NOT implemented

# What can be done with root?
You can do some essential things:
- Bypass Google's Play Integrity checks, unlocking some apps, RCS messaging and GPay
- Use apps that require root
- Undervolt with an appropriate kernel (not supported)

# Disclaimer
Having root access on your phone can be dangerous. Only install trusted modules. There have been many instances of malicious root modules wiping or bricking devices, so be careful. 