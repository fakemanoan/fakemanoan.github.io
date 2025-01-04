---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Capturing logcats"
---
[ <-- Back](../)
# Capturing Logs for bug reports
Sometimes you may experience a problem that is reoccuring or unpredictable. Developers may ask for logs from your device in order to help them fix the problem.

# Pre-requisites
- USB drivers
- USB cable
- ADB installed on your PC
- Device boots into an OS
- Place to upload your logs

# Steps to get logs
## 1. Make sure you have Android Debug Bridge (ADB) installed on your computer and it is functioning. 
This is essential to retrieving logs. Without adb installed on a PC, we cannot proceed. Follow this guide here: [https://www.xda-developers.com/install-adb-windows-macos-linux/](https://www.xda-developers.com/install-adb-windows-macos-linux/)

## 2. Enable developer options on your phone
Navigate to settings, about phone, android version.

Tap the build number 5 times quickly. If you are successful it should say "you are now a developer" at the bottom of the screen

## 3. In developer options enable ADB debugging 
Navigate to Settings, System, Developer Options

Turn on USB debugging. You might as well turn on rooted debugging too, as sometimes you may need this

## 4. Plug your device into your PC
You may get a pop up on your device about ADB. Allow remote debugging always for your PC

You can test to see if adb works by typing 

``
adb devices
``

You should see your device listed. If it says "offline", check your USB connection and you enabled debugging in developer options.

## 5. Replicate the bug 
Use your phone normally until you encounter the bug you are having. After the bug occurs you can now capture logs. You can do this by typing the command:

``
adb logcat -db all > FILENAME
``

Replace FILENAME with an appropriate name. This command will output all the logs from the Android system into a file called FILENAME whereever you have your console open.

## 6. Upload these logs to a private location
Ensure that the developer has access to the file, otherwise the logs won't really help them diagnose the problem

Sometimes bugs can take a long time to fix, so be patient and co-operative. If you have found a solution to a problem, detail your fix. Sometimes it may help. 

After the developer has obtained the logs, you may want to delete the logs after sometime, as there may be sensitive information in the logs depending on what you are debugging. 