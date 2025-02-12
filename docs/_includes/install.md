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
- Select Wipe
- Select Advanced Wipe, and select Cache, System, Data. **MAKE SURE YOU HAVE A BACKUP**
- Confirm to delete when prompted
- Transfer your files you downloaded to the S6 via USB
- Go back to TWRP home and select install
- Select the LineageOS Zip File and wait for it to flash
- Install extras if you have any in the same way
- Reboot system (don't install TWRP app)
- Wait for first boot, can take about 5 mins

# Troubleshooting
### Device not showing in Odin
- Make sure your USB cable has working data. Confirm this by transfering a file to your phone in Android.  
- Make sure you have the right USB drivers installed from the official Samsung website  
- Make sure you have the correct Odin version
- Make sure you run Odin with administrative privelleges 

### Missing TWRP after flashing LineageOS
You may have selected "update recovery" when setting up your phone
- In LineageOS, navigate to Settings. Then go to System -> Updater 
- Select the 3 dots in the top right, and go to Preferences
- Disable "Update Recovery"
- Re-flash TWRP in Odin following the TWRP install instructions on [this page](/downloads/twrp)

### Google Play Store/Google Services has no network access
This is commonly done because you did not follow the guide properly.
- Ensure you flash Gapps BEFORE you boot
- If you accidentally booted then installed Gapps, you can do a factory reset in TWRP to fix this issue.
