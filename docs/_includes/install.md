# Install guide
**WARNING: THIS PROCESS WILL WIPE YOUR DEVICE CLEAN. BACKUP ANY IMPORTANT FILES NOW.**

## Pre-requesites 
- A Windows Computer with Samsung USB drivers 
- A USB cable with data capabilities 
- Device charged to at least 60% 

## Step 1 - Install TWRP
- Download the latest TWRP from [here](/downloads/twrp). Ensure you use this version or TWRP will hang
- Download Odin
- Enable developer options on your device and enable OEM unlocking if present
- Power off your device and boot into Odin mode (Power + Volume Down + Home)
- Flash the TWRP tar image in the AP slot in the Odin application
- Reboot into TWRP Recovery (Power + Volume Up + Home)
- Swipe to allow modifications
- Create a full backup

## Step 2 - Install the ROM
- Boot into TWRP Recovery (Power + Volume Up + Home)
- Download the latest LineageOS zip and any extras, like Gapps
- Select Wipe
- Select Advanced Wipe, and select Cache, System, Data
- Confirm to delete when prompted
- Transfer your files you downloaded to the S6 via USB
- Go back to TWRP home and select install
- Select the LineageOS Zip File and wait for it to flash
- Install extras if you have any
- Reboot system (don't install TWRP app)
- Wait for first boot, can take about 5 mins

## Troubleshooting
### Device not showing in Odin
- Make sure your USB cable has working data. Confirm this by transfering a file to your phone in Android.  
- Make sure you have the right USB drivers installed from the official Samsung website  
- Make sure you have the correct Odin version
- Make sure you run Odin with administrative privelleges 