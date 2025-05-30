---
layout: default
title: "TWRP Downloads"
---
[ <-- Back](/)

# TWRP 3.7.0-9.0
TWRP (Team Win Recovery Project) is a custom recovery for Android Phones. It allows us to do advanced things, such as install Custom ROMs, take backups, and modify the file system on our device.

The TWRP version maintained on the official website is outdated, and has issues for running newer versions of Android.

This is my version updated of TWRP. It is required to have the following features:
- new TWRP version with updated kernel
- working Android 12+ support, older TWRP versions hang
- working OTA updates

Other TWRP versions that are 3.7.0-9.0 will work, however only **MY** version of TWRP will have working OTA support currently

# Downloads
{% capture install_content -%}
Make sure you download the correct TWRP version, or else you may have inverted touch, boot issues or won't be able to install the correct ROM for your device. If your device is not listed, DO NOT FLASH THESE VERSIONS.
{%- endcapture %}

{% include alerts/warning.html content=install_content %}

## Samsung Galaxy S6 (zeroflte)
- [.IMG file](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9.0_19012024/TWRP_3.7.0-9.0_zeroflte_19012024.img)
- [.TAR file](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9.0_19012024/TWRP_3.7.0-9.0_zeroflte_19012024.tar)

## Samsung Galaxy S6 Edge (zerolte)
- [.IMG file](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9.0_19012024/TWRP_3.7.0-9.0_zerolte_19012024.img)
- [.TAR file](https://github.com/fakemanoan/TWRP-Releases/releases/download/TWRP_3.7.0-9.0_19012024/TWRP_3.7.0-9.0_zerolte_19012024.tar)

<br>

# Installation Guide
{% capture install_content -%}
As always with custom ROMs, these builds come with NO WARRANTY. Proceed with caution.
{%- endcapture %}

{% include alerts/alert.html content=install_content %}

## Step 1: Download the required files
You will need
- TWRP file linked above. If your device is not listed then you can download from [here](https://drive.google.com/drive/folders/1gAlPsZIkYM-XYWu-JWJCDgwJ-60h0Ss2).
- Windows PC (is possible on Linux too, but wont cover that here)
- Odin 3.13.1
- Samsung USB drivers
- USB 2.0 cable with data

You will also need a device with a working Home button and volume buttons. If you don't, then unfortunately there is no easy way to proceed.
Install Odin and the Samsung USB drivers. Then you can continue

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

If you would like to build your own TWRP, the source code is available on the samsungexynos7420 GitHub.