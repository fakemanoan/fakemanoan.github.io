## 24.09.2024
- Sync with LineageOS sources
- Sept 2024 ASB
- Rebase to lineage-19.1 branch

## 28.08.2024
- Sync with LineageOS sources
- Merge August 2024 ASB
- Swap to 18.1 based kernel - cleaner commit history
- Reduce max GPU clock speeds for cooler temperatures
- Remove build_soong patch, fix up SLSI warnings

## 11.08.2024
- Sync LineageOS sources
- Merge July 2024 ASB
- Builds are now signed. This will allow you to bypass Play Integrity if you use PIF. This is a migration build, so to recieve future updates, you must flash this first if you are coming from older builds.
- Update device fingerprints
- Attempt at fixing dual sim support (again)
- Remove some debug info
- Swap to skiagl renderer from threaded

## 17.05.2024
- Sync LineageOS sources
- Merge May 2024 ASB
- Disable kernel tracing
- Update SDFat version to 2.4.5
- Fixed wireless charging not being correctly detected
- Use dual sim modem pdata on all variants
- Tweak interactive power profiles slightly

## 14.04.2024
- Sync with LineageOS sources
- April 2024 ASB
- Swap to Android 13 Linaro BSP (credits to k9100ii for reimplementing hwc1)
- Reclaim 210MB of RAM from hack we no longer need
- Fixed UI lag when memory pressure is high
- Ported over CMA/MM stuff from 7580, way better multitasking
- Fixed AOD not working
- Enable stack protector

## 13.03.2024
- Synced with LineageOS sources
- ASB March 2024
- Official Lineage support for MicroG
- Swap to d2s RIL blobs, better compatability and call quality
- Build libfimg5x from old BSP
- Fix few kernel errors

## 21.02.2024
- Synced with lineageos source
- Feb 2024 security updates
- Swapped to a rebased kernel, cleaner commit history
- Added some more patches to reduce a few errors
- Small undervolt, shouldnt change too much
- DT2W is more consistent
- Ported bypass charging to the S6
- Use S6 brightness mapping
- No more impl composer

## 19.01.2024
- Sync with LineageOS sources
- Merged Jan 2024 ASB
- Build HWC services
- Build HDMI instead of HDMI_dummy
- Fixed kernel build parameters
- Backport some decon changes from exynos 8890
- Backport some BTS features from exynos 8890
- Re-add DT2W (Although it is a bit buggy at this time)
- Fixed AOD not working
- Added OTA support. Please read the footnote regarding this
- Down rev to passthrough 2.1 composer for now as a test
- Move to 2048 xhdpi dalvik config. 4GB config was a bit too aggressive
- Set ZRAM size to a static 1.5GB
- Swap to more oreo blobs and fw files from A810S
- Fixed HEVC encoding
- small kernel updates

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