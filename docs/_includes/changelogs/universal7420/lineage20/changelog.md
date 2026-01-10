## 10.01.2026
- Sync with LineageOS source
- ASB 01-2026
- disable AFBC
- Update kernelsu to 32264 (credits to @backslashxx)
- Enable UIDGID_STRICT_TYPE_CHECKS to make porting kernelsu easier
- Updates to Kbuild
- Add cross_rename support, missed in renameat2 patches
- Backport new shrinker and move lmk over to it
- Swap mali r22p0 driver to new shrinker API
- Remove fake command line, can be spoofed with root tools
- int_sqrt optimizations
- Backport some mm changes/fixes from android-3.18 common kernel and 8890
- Hook up ZSMALLOC_STAT and enable it
- Enable PGTABLE_MAPPING
- Enable INCREASE_MAXIMUM_SWAPPINESS
- Enable BALANCE_ANON_FILE_RECLAIM
- Add some missing sched updates I missed
- Set CMA size to 24 on S6/S6e only
- revert new vmalloc changes
- GPU: use interruptable wait for lower latency
- Backport mm/cma.c from 8890 kernel
- Backport process_reclaim but with new shrinker in mind
- Add defconfig option for vmpressure_medium levels
- Remove libsensor patch - ship with pre compiled modded one
- Rename libril to libril-samsung to avoid collisions
- Implement DO_ONCE and therefore remove some hacks from BPF Implementation

## 29.11.2025
- Sync with LineageOS source
- Merge ASB 
- Compile kernel with clang
- Backport MAX_DIRTY_THRESH_PAGES from exynos 9810
- Allow DIRECT_RECLAIM_FILE_PAGES_ONLY and others to be used with SWAP
- Backport PAGE_BOOST from 7885
- Backport aio F_FS driver from A600F Q. Hence remove adb patch
- Backport ION from A600F Q.
- Backport new vmalloc for "large performance benefits"
- Backport pidfd sys call
- KernelSU update to 12128
- Tweak some vm values for better swap behaviour hopefully
- Enable ARM framebuffer compression, maybe for better HWC performance
- Update cryto modules in kernel
- Build kernel optimizations for cortex-a53

## 26.08.2025
- add some more arm64 changes
- enable BPF JIT properly
- add f2fs support for /data and /cache (requires 9-1 TWRP to work - properly, which will be released shortly)
- backport adaptive gpu power governor
- backport process_reclaim
- few misc mm changes
- enable dm_verity
- update kernelsu to 12107 (credit @backslashxx)
- update ion
- update arm64 vdso

## 25.06.2025
- Revert Cgroup v2 and kernfs changes
- Add arm64 changes from 3.14/3.18
- Enable arm64 BPF JIT
- Update kernelsu to 12103 (ty to @backslashxx)
- Add undervolting support (requires root)
- fix mm patches i missed
- binder changes from 4.4
- misc changes
- swap to lmkd

## 11.06.2025
### Device tree:
- Unify W8/T and F/S/I/K models - 1 zip for all
- Audio HAL now dynamically swaps to ES path depending on device bootloader
- Decommonise audience firmwares
- Decommonise audio firmwares
- Decommonise sensors
- Use proper NFC firmware for Note5/S6E+
- Build CPBoot daemon v1 from source
- Fix up some SEPolicy compile errors due to LF vs CRLF
- Fix SELinux denials
- Note 5 devices correctly identify their models
- S6 edge can now properly disable touchkeys thanks to a new node in the kernel
- Decommonise wifi parameters, and add support for swlan0 for note 5/s6e+ (will probably need to eventually rename this to wlan1)
- Use non-legacy wifi hal
- Build NFC HAL from source
- WPA3 now downgrades to WPA2 (our kernel and firmware dont support SAE)
- S6 edge+ support
- add A810F fingerprint blobs - this removes a hack in the HAL that isnt supported in later versions
- completely remove ebpf and cgroup patches, these are no longer needed (looking to remove more)
- swap to threaded render back-end instead of skiagl - seems to be gralloc issues? no idea
- Latest ASB available

### Kernel changes:
- Rebase and redo from scratch for a cleaner commit history
- Create unified dts files
- Fix available memory in /proc/meminfo showing discrepancies sometimes
- Disable more debugging to stop dmesg spam
- add back samsung customizations to sdcardfs and ecryptfs
- Properly fix IOVM allocation being broken causing lag sometimes in HWC
- Add more drivers to power_efficient_wq
- Increase display QoS
- Port some CMA_PINPAGE_MIGRATION features from 8890
- Port LARGE_DIRTY_BUFFER from 8890
- Port MEMCG_FORCE_SWAPPINESS from 8890
- account for unmovable pages in LMK
- Port ext4 from 3.18
- Port JBD2 from 3.18
- port fusefs from 3.18
- Add p9220 wireless charger firmware
- convert all firmwares to ihex
- remove hacks from kbuild
- Allow hall effect sensor detection to be reversed via config option
- Allow Play Integrity spoofing boot cmdline params to be disabled via option
- port arm64 features, like hardened user copy
- port bcmhd4359_100 from 8890 for note 5/s6e+ - allows concurrent hotspot and wifi connections
- binder/android updates
- f2fs updates
- alsa updates
- net updates
- Block/loop patches
- remove some of samsungs mm modifications
- disable FIPS/FMP, was broken anyway
- Port kern/sysfs from 3.18
- Add changes from 3.18 to cpuset/mm
- Use monotonic boottime for the camera (@K9100ii credit)
- use bcmhd_1_77 for BCM4358 for s6/s6e - newer oreo driver, should work a bit better
- port kernelsu (credit to @backslashxx)
- port overlayfs from 4.1 (credit to @backslashxx)
- port over cgroup v2
- port over eBPF
- Spoof kernel version to bypass version restrictions on art, memfd, bpf, etc

## 12.12.2024
- Sync with Lineage source
- Merge Dec 2024 ASB
- Note 5 test build

## 11.11.2024
- Sync with Lineage source
- Merge Dec 2024 ASB
- Note 5 test build

## 24.11.2024
- Sync with lineage sources
- November 2024 ASB
- Network traffic monitoring fixed
- Kernel updates
	- locks patches
	- rcu patches
	- ebpf backport (credits to acroreiser and rootfan for the patches)
	- ext4 updates
	- mm updates
	- add "available memory" to /proc/meminfo for lmkd
	- other misc changes

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