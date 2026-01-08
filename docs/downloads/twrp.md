---
layout: default
title: "TWRP Downloads"
---
[ <-- Back](/)

# TWRP 3.7.0-9.1-fakeman
TWRP (Team Win Recovery Project) is a custom recovery for Android Phones. It allows us to do advanced things, such as install Custom ROMs, take backups, and modify the file system on our device.

The Official TWRP is outdated and lacks features for my ROMs. Because of this, I have decided to create my own images.

Notable features:
- updated android-9.0 branch
- working Android 12+ support, older TWRP versions hang
- working OTA updates
- updated kernel
- F2FS supported
- Potentially more features in the future, like treble/GSI support

# Downloads
{% capture install_content -%}
Make sure you download the correct TWRP version, or else you may have inverted touch, boot issues or won't be able to install the correct ROM for your device. If your device is not listed, DO NOT FLASH THESE VERSIONS.
{%- endcapture %}

{% include alerts/warning.html content=install_content %}

## Samsung Galaxy S6 (zeroflte)
- [Download (.img file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zeroflte.img)
- [Download (.tar file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zeroflte.tar)

## Samsung Galaxy S6 Edge (zerolte)
- [Download (.img file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zerolte.img)
- [Download (.tar file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zerolte.tar)

## Samsung Galaxy S6 Edge+ (zenlte)
- [Download (.img file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zenlte.img)
- [Download (.tar file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_zenlte.tar)

## Samsung Galaxy Note 5 (noblelte)
- [Download (.img file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_noblelte.img)
- [Download (.tar file)](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9-2/TWRP_3.7.0-9-2-fakeman_noblelte.tar)

<br>

# Installation Guide
{% capture install_content -%}
As always with custom ROMs, these builds come with NO WARRANTY. Proceed with caution.
{%- endcapture %}

{% include alerts/alert.html content=install_content %}

## Step 1: Download the required files
You will need
- TWRP .tar file
- Windows PC (is possible on Linux too with heimdall, but wont cover that here)
- Odin 3.13.1
- Samsung USB drivers
- USB 2.0 cable with data

You will also need a device with a working Home button and volume buttons. If you don't, then unfortunately there is no easy way to proceed.
Install Odin and the Official Samsung USB drivers. Then you can continue

### Step 1.5: Enable USB debugging and OEM unlocking
Enable developer options on your device, and then in developer options, enable USB debugging and (if present) OEM unlocking.

## Step 2: Reboot into Download mode
Completely power down your device so that it is off.

You can then hold the Power button, Volume Down button and the Home button ALL AT THE SAME TIME. You should see a teal/green screen.

Read the information, then press Volume up once you are ready to continue

## Step 3: Open Odin and flash TWRP
Connect your phone to your PC. Then you can open the Odin program.

{% capture install_content -%}
On some versions of Windows, you may need to open Odin as Administrator so the program can detect your device
{%- endcapture %}

{% include alerts/warning.html content=install_content %}

Press the "AP" BUTTON, and then select your TWRP .tar image you downloaded.

Under the Options tab, de-select "Auto reboot". We will need to reboot the phone ourselves.

## Step 4: Flash TWRP
Once you are ready to go, select the "Start" button. Do not unplug your device!

Once it has a green box saying "Success!", we can hold the Volume down and Power buttons at the same time again for 5 seconds to reboot the device.

Once the screen has turned black, hold Home + Volume Up + Power button all at the same time. This will reboot into TWRP. If you boot into the OS, there is a chance the recovery will reset to the stock one.

You should see a TWRP screen.

{% capture install_content -%}
At this point we can Swipe to allow modifications, and we can install custom ROMs or root access 
{%- endcapture %}

{% include alerts/info.html content=install_content %}

If you would like to build your own TWRP, the source code is available on the samsungexynos7420 GitHub (look for TWRP_ repos).