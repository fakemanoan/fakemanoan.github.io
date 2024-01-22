## 19.01.2024
- Synced with LineageOS sources
- Android security update to December 2023
- Swapped to a temporary stable kernel, old one had a few stability issues
- Implemented VDSO32 from Nvidia tegra 3.10 kernel
- A few changes to CPU boosting
- Hidden DT2W function added (still needs some work to be perfect, but you can activate via sysfs node if you really want it)
- Scrcpy (and similar apps) fixed and working due to kanged usb config from 8890q
- Changed dalvik cache settings to predone ones
- Better multitasking
- Swapped to libutils-v32 for camera blobs
- Added back lifevibe blobs and audience firmwares
- Enabled more audio effects
- Volume control is more granular when using buttons
- Swapped back to threaded renderbackend from skiaglthreaded - due to gralloc changes breaking it
- Disabled AOSP night and dim display - Superior LiveDisplay functions have returned
- Uprev LiveDisplay to 2.1
- Vibrator settings changed to sliders
- Dual sim detection should be working
- Cleaned up device tree
## 04.01.2024
- Synced with LineageOS sources
- Android security update to December 2023
- Swapped to a temporary stable kernel, old one had a few stability issues
- Implemented VDSO32 from Nvidia tegra 3.10 kernel
- A few changes to CPU boosting
- Hidden DT2W function added (still needs some work to be perfect, but you can activate via sysfs node if you really want it)
- Scrcpy (and similar apps) fixed and working due to kanged usb config from 8890q
- Changed dalvik cache settings to predone ones
- Better multitasking
- Swapped to libutils-v32 for camera blobs
- Added back lifevibe blobs and audience firmwares
- Enabled more audio effects
- Volume control is more granular when using buttons
- Swapped back to threaded renderbackend from skiaglthreaded - due to gralloc changes breaking it
- Disabled AOSP night and dim display - Superior LiveDisplay functions have returned
- Uprev LiveDisplay to 2.1
- Vibrator settings changed to sliders
- Dual sim detection should be working
- Cleaned up device tree

## 13.10.2023
- Synced with lineage sources
- Oct 2023 ASB
- Swapped to skiaglthreaded as the render backend, as well as skiagl for hwui
- Low RAM tweaks
- Improved GPS stability
- Improved idle power consumption
- Improved battery life

## 28.09.2023
- Synced with LineageOS sources
- September 2023 ASB
- Fixed edge camera not working
- Changed default TCP scheduler to bic
- Enabled LCD doze mode
- Fingerprint when screen off should be fixed (ivan_meler credit)
- Swapped to camera 2.5 service

## 13.09.2023
- Moved away from legacy wifi HAL
- Added missing wifi config files
- UI performance improved, same changes as android 12
- 15+% improvement in some benchmark scores
- Faster app launch times
- Fixed camera not being able to take pictures
- Stop logcat spam of debug stuff
- Maybe fixed BT audio in calls? (need testers!)
- Reverted headphone gain change in mixer_paths - too quiet for people

## 24.07.2023
- Initial Edge release
- Synced with los (july 2023 security)
- Swapped back to lineage fingerprint flag (FP shouldnt be triggered when screen off)
- Added Lineage Health HAL - battery charge limit
- HWC tweaks
- 8890 kanged auto brightness mapping
- Android Go tweaks

## 07.07.2023
- Synced with LineageOS sources
- New A810F based kernel with a bunch of additions - a lot of patches were from k9100ii's 7580 trees
- Swapped to r22p oreo driver finally, issues seemed to be with a bad gralloc implementation
- OMX video should be fixed
- More under the hood tweaks, should be more responsive

## 15.05.2023
- Initial release for flat models