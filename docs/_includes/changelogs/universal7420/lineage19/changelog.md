## 02.12.2024
- Sync with Lineage
- Nov 2024 ASB
- Kernel updates
    - locks patches
    - rcu patches
    - ebpf backport (credits to acroreiser and rootfan for the patches)
    - ext4 updates
    - mm updates
    - other misc changes

## 25.10.2024
- Merge October 2024 ASB
- SEPolicy updates, still no enforcing - working on this!

## 20.10.2024
- Sync with LineageOS sources
- Sept 2024 ASB
- Kernel updates
    - Add "available memory" to /proc/meminfo for lmkd
    - Add cpufreq attributes
    - Select lowest frequency in interactive governor for a bit of power savings
    - Bring in some changes from 7580 gud
    - Fix invalid mif values in mali frequency table
    - Resolve a few compilation warnings
- More SEPolicy changes - still no enforcing just yet

## 15.05.2024
- Sync LineageOS sources
- Merge May 2024 ASB
- Disable kernel tracing
- Update SDFat version to 2.4.5
- Fixed wireless charging not being correctly detected
- Use dual sim modem pdata on all variants
- Fix memory leak in linaro BSP (credits to K9100ii for work on his BSP)
- Move all BSP packages to /vendor (was reverted previously)
- Tweak interactive power profiles slightly
- Address some SELinux denials (still permissive though)

## 10.04.2024
- Sync LineageOS sources
- Merge April 2024 ASB
- Fixed selfie cam not working on Note 5
- Reclaim 210MB of RAM from hack we no longer need
- Fixed UI lag when memory pressure is high
- Ported over CMA/MM stuff from 7580, way better multitasking
- Fixed AOD not working
- Dual sim support (needs testing)
- Enable stack protector
- Remove some lights debugging messages

## 11.03.2024
- Synced LineageOS sources
- March 2024 ASB
- Official Lineage Support for MicroG
- Swapped to d2s RIL blobs, better call stability, less hacks
- Uprev live display to 2.1
- Initial SEPolicy (still permissive though)
- Some SafetyNet "Strong" device parameters spoofed
- Fix some kernel errors

## 01.03.2024
- Initial Note 5 Release

## 20.02.2024
- Synced lineage os sources
- feb 2024 ASB
- Rebased kernel, cleaner commit history
- DT2W should work more reliably
- UI performance improved
- Temporarily revert AOD changes
- Use S6 brightness nit mapping (we were using S7 one before)
- 2.5 camera service uprev

## 26.01.2024
- Synced with LineageOS sources
- Jan 2024 security updates
- Swap to a temporary kernel for now
- Correct kernel offsets
- Initial VDSO32 support
- Disabled exynos memory compression
- Disabled slow mode
- Swapped to r22p0 oreo driver
- Improved graphics performance
- Backport some changes from 8890 kernel
- Tweaked CPU boosting behaviour
- Low RAM optimizations
- Better utilise our 3GB of RAM for apps
- Updated HWC implementation
- Update cpusets
- Override build fingerprints
- Move to prebuilt secnativefeature
- Update some blobs to oreo
- Misc changes
- Clean up samsungexynos7420 sources
- Add lineage 20 health - battery limit backported + bypass power mode
- Build libfimg from old bsp
- Add OTA support
- Fixed SCRCPY and similar apps
- More granular control for volume
- Fixed AOD not working
- Added DT2W

## 12.09.2023
- Synced with lineageos sources
- September 2023 ASB merged
- Revert kernel changes from last build
- Fix edge build not installing for people, small error on my part
- dimens updated
- New installs now have a friendly default device name. ie Galaxy S6, or Galaxy S6 Edge
- Tree cleanup
- Camera2 API regression should be resolved
- BT audio in calls improved? (need testers!)
- Reverted headphone gain change

## 20.08.2023
- Synced with Lineage OS sources
- Android August 2023 security patch
- Added signature spoofing support
- UI performance should be slightly better
- HWC tweaks/changes, see how it goes
- Changed default CSC to 5, was previously set at 4 incorrectly during linaro BSP transition
- Ramdisk cleaned up and refined, still more work to be done
- Power button y location set, so fading from AOD looks better
- Reduced ZRAM size to 1.3GB
- Enabled LifeVibe blobs to attempt to reduce echo more in calls. Might sound better/worse, who knows
- Retuned power profiles a bit, might be better/worse, who knows
- Default undervolt of all CPU clusters by 37.5mV
- Removed device fingerprint CTS stuff for now (root was needed to pass safetynet anyway)
- Cleaned up overlays
- Cleaned up some unnecessary patches
- Tweaked dex2oat values to be more inline for 3GB devices
- Disabled some kernel logging of certain things, just because its annoying
- Other small kernel improvements, not worth noting

## 19.07.2023
- Synced with LineageOS sources (June/July 2023 security releases)
- New kernel based off A810F sources - appears to be stable in day to day use. Any issues report in the thread
- HWC changes - just to try
- Haptic text cursor support
- Kanged 8890 display nit mapping
- Boot animation shows earlier now, small improvement to boot times
- IPA control temp is now in the power HAL. Boosts to 120 for a second on app launches (like stock). Lowers to 45 on power saver.

## 07.05.2023
- Synced with LineageOS sources (May '23 security patch)
- Swapped to linaro BSP for some HWC components
- Provides updated code for our device (better UI/performance)
- Update precompiled OMX blobs (linaro ones dont work currently), modified to work in vendor/
- Move most stuff to /vendor (finally)
- Set minimum clock speed in non-power saver mode to 400MHz for A53 cores
- GPU now looks for hi-speed load
- Other misc kernel improvements
- Update seccomp policies
- Memfd legacy patches added (as we arent on kernel 3.18 or newer)
- LPM kanged from 8890q
- Misc changes to props

## 12.04.2023
- You must perform a clean flash. Backup your data using your preferred method, or else you wont be able to unlock your device.​
- Synced with LineageOS source (April 2023 security)
- Reworked the HWC implementation - noticeable improvement to smoothness
- All 7 layers are now working
- More HWC components built from BSP source + extra flags
- Using A810F Gatekeeper blobs - MDFPP implementation from software
- Less random errors in logcat
- Build fingerprints overridden to latest stock nougat ones
- L3 widevine DRM support, some DRM content should work now
- Zswap no longer built in the kernel. We don't need it.
- In kernel low memory killer is no longer built
- Fixed FIPS compilation
- Default voltage offset of -37.5mV on the CPU
- Upped sustained clock speeds hint in powerhints.json

## 22.02.2023
- Synced with LineageOS sources (March 2023 security updates)
- Fixed regression where bluetooth audio crackles when screen is off (core hotplugging is disabled for now)
- Fixed VP9 video decoding in apps. We now have more quality options on YouTube. Our hardware can't do 4K60, so only 4K30
- ZRAM settings kanged from exynos 7580 (75% of RAM is ZRAM now). This should be better for general usability
- Thanks to enesuzun2002 releasing the BSP, we can now build HWC components from source. Shouldn't change too much for now, but its nice

## 25.02.2023
- GPS works now
- Fixed regression where mobile data wouldn't work (need different patches for netd/bpf for some reason)
- HRM/SPO2 works semi-properly now due to a missing SPO2 permission (taken from universal5433).
- ZRAM reduced to 800mb for now

## 15.02.2023
- Synced with LineageOS sources (Feb 2023 security update)
- Back on Nougat kernel for now
- So edge models should be able to disable hw buttons without issue
- Added FB notifier for touchscreen and touchkey - touchkeys no longer vibrate when screen is off
- Added CPU/GPU voltage control. Use hkTweaks to undervolt. (at your own risk)
- Added BFQ i/o scheduler
- Added Dynamic F-Sync (from anans cronos kernel)
- Wireguard VPN support
- Battery store_mode support
- Hwbinder for sensors, memtrack, renderscript, GNSS
- uprev BT audio hal to 2.1
- Fixed headphone jack being too loud
- AdvancedDisplay added
- Logs no longer spammed with errors about CPUs being online. Moved to a less jank way of disabling cores on power saver. You can control amount of cores online by editing the value in /sys/power/cpucore_max_num_limit (8 = all cores online, 4 = all big cores disabled etc)

- Misc changes:
- Source code moved to samsungexynos7420. Please build from there.
- 7420_patches cleaned up, a lot werent needed.
- Using protobuf 2.6 now instead of 2.4 - precompiled and included in vendor
- Newer aptX from crosshatch
- secril blobs from latest official nougat
- ZRAM settings changed a bit, nothing big

## 12.12.2022
- Synced with lineage sources - android december security update
- Removed AudioFX as a test

## 22.11.2022
- Synced with LineageOS sources, we have novemeber security updates
- UI performance dramatically improved due to prebuilt HWC components
- Bluetooth audio fixed, we were building 64bit HAL for some reason
- ZRAM values tweaked
- Added experimental aptX
- Added experimental freeform windows
- Core hotplugging disabled, causes issue with BT audio when screen is off
- Swapped to LE video codecs for now
- New power saver mode - 4 small cores, 2 big cores, tweaked frequencies (jank implementation lol)
- OpenCL fixed
- Fixed GPS rollover bug

## 08.10.2022
- Fixed S6 Edge not booting (weird kernel glitch)
- Modified powerhints.json

## 07.10.2022
- Synced with LineageOS sources
- Swapped to EQ1 kernel based on S6 Nougat firmware. However due to last minute issues, only necessary features were added.
- Added and enabled ZRAM with lz4, improves general usability
- Graphics should be slightly smoother
- AOD now has acceptable brightness, better implementation later
- Added Heart Rate Monitor permission
- Switched to new Pixel Power HAL from hw/samsung
- Fingerprint reader fixed (ty @ArmashOnXDA for the help)
- Added basic vibration intensity control
- Overall system responsiveness improved
- G925F touch key disabler should work properly now
- USB tethering fixed

## 28.08.2022
- Initial G925F release
- AOD enabled
- Keydisabler is working, meaning on-screen buttons and gestural navigation can be selected
- Reduced default display density to compensate for A12's new UI

## 23.08.2022
- Initial Release for flat models