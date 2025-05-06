# Install guide
**WARNING: THIS PROCESS WILL WIPE YOUR DEVICE CLEAN. BACKUP ANY IMPORTANT FILES NOW.**

## Pre-requesites 
- A Windows Computer with Samsung USB drivers 
- A USB cable with data capabilities 
- Device charged to at least 60% 

## Step 1 - Install TWRP
- Download the latest TWRP from [here](/downloads/twrp). Ensure you use this version or TWRP will hang
- Follow the instructions on that page

## Step 2 - Install the ROM
- Download the latest LineageOS zip and any extras, like [Gapps](/downloads/mindthegapps) or Magisk
- Boot into TWRP Recovery (Power + Volume Up + Home)
- Select Wipe -> Advanced Wipe and select Cache, System, Data. **THIS WILL DELETE YOUR CURRENT OS**
- Confirm to delete when prompted
- Transfer your files you downloaded via USB
- Go back to TWRP Home and select "Install"
- Select the LineageOS Zip File and wait for it to flash
- Install extras AFTER LineageOS is done (GApps, root, etc)
- Reboot system (don't install TWRP app)
- Wait for first boot, can take about 5 mins

# Troubleshooting
### Google Play Store/Google Services has no network access
This is commonly done because you did not follow the guide properly.
- Ensure you flash Gapps BEFORE you boot
- If you accidentally booted then installed Gapps, you can do a factory reset in TWRP to fix this issue.
