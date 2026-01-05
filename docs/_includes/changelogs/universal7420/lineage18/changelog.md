## 05.01.2026
- Update KernelSU to 32181 (credits to @backslashxx)
- Backport AIO f_fs from A600F Q (but use legacy adb as it is supported in los18)
- Add HWUI props, maybe better who knows
- Remove fake command line, can be spoofed with root tools
- Add showmem_extra from A600F Q
- Add Ion from A600F Q
- Updates to Kbuild
- Add some missing sched updates I missed
- Backport cpu_interactive_speedchange_task (credits to @ananjaser1211 from cronos_7420)
- Backport more arm64 patches
- Hook up ZSMALLOC_STAT and enable it
- Backport PAGE_BOOST from 7885
- Backport some mm changes/fixes from android-3.18 common kernel and 8890
- percpu updates
- block updates
- int_sqrt optimizations
- Backport shrinker and move lmk over to it
- GPU: use interruptable wait for lower latency
- Backport mm/cma.c from 8890 kernel
- Enable UIDGID_STRICT_TYPE_CHECKS to make porting kernelsu easier
- Enable PGTABLE_MAPPING
- Enable DIRECT_RECLAIM_FILE_PAGES_ONLY
- Enable INCREASE_MAXIMUM_SWAPPINESS
- Enable BALANCE_ANON_FILE_RECLAIM
- Set CMA size to 24 on S6/S6e only
- Backport process_reclaim
- Add defconfig option for vmpressure_medium levels
- remove SCFS
- Enable ext4 posix
- enable qfmt_v2
- Enable MPTCP on all devices, just because
- Enable some misc drivers

## 07.09.2025
- Revert to pre kernfs kernel for now
- Backport some sched patches
- Backport some ion patches
- Enable schedstats
- update kernelsu to 12107
- Change decon to FIFO
- Increase MIF frequency in decon driver
- backport some QoS/PM features
- m2m1shot from 8890
- compile kernel using clang
- add f2fs support
- backport renameat2
- arm64 updates

## 19.06.2025
- Update KernelSU to 12103 and revert a few unnecessary changes (ty to @backslashxx)
- import/backport some arm64 changes from 3.14/3.18
- optimize for performance (-O2, mtune etc)
- stop mediaserver selinux denial spam
- add back undervolting - requires root and undervolting app (eg hKtweaks)
- swap zenlte to unified DT - forgot to wire it up - woops!
- add battery extender hal

## 09.06.2025
- Block/loop patches
- remove some of samsungs mm modifications
- disable FIPS/FMP, was broken anyway
- misc changes
- Add 3.10 kernelsu implementation (big ty to backslashxx)
- add overlayfs from 4.1 (big ty to backslashxx)
- swap to oreo A810F fingerprint blobs, remove some hackery (you may need to remove and re-add your prints)

## 07.05.2025
- Fix up invalid GPIO pinout causing missing call audio in NA variants
- Enable a few more kernel options
- Fix up LMK being a bit too lenient
- Enable enforcing on S6 Edge+ and subsequently label the appropriate paths
- Link up OTA URL for S6 Edge+ for upcoming TWRP release
- other misc kernel changes
- fix up invalid audio paths causing video recording to sometimes fail

## 02.05.2025
- revert cma change
- preliminary zenlte (S6 edge+) support : PLEASE PROVIDE LOGS SO I CAN ENABLE SELINUX!
- correct incorrect mixer paths reference in audio hal
- correct headers in macloader to point to correct path

## 01.05.2025
- Fix Fingerprint TEE denials (again...)
- Fix issue where Edge devices couldnt detect a SIM
- Use 24MB CMA allocation
- Alter mixer_paths for audience models
- misc: move hotplug govenor to samsung soc folder in kernel - nothing should change from this
- use speed-profile for server compiler filter
- add some android go optimizations
- fix up wpa_supplicant overlays from ages ago
- add armnn

## 28.04.2025
- Address fingerprint tee denials
- Add WifiOverlay and set default device hotspot names
- use bcmhd_1_77 for BCM4358 for s6/s6e - newer oreo driver, should work a bit better
- Use non-legacy wifi hal
- Build NFC HAL from source
- Set kernel to 300hz
- use monotonic boot time for camera (k9100ii credit)
- disable tracing
- disable more logging
- add kernfs from 3.18
- updates to sysfs from 3.18
- updates to cgroup from 3.18
- updates to cpuset from 3.18
- updates to mm from 3.18
- wpa3 autoupgrade fixed - if you are on a wpa2/wpa3 mixed network it should work properly now
- mixer_paths fixes
- misc overlay changes

## 08.04.2025
Device tree:​
- Unify W8/T and F/S/I/K models - 1 zip for all
- Audio HAL now dynamically swaps to ES path depending on device bootloader
- Decommonise audience firmwares
- Decommonise audio firmwares
- Decommonise sensors
- Use proper NFC firmware for Note5/S6E+
- Build CPBoot daemon v1 from source
- Use mali r15p0 blobs from note 5 (slightly newer)
- Fix up some SEPolicy compile errors due to LF vs CRLF
- Fix audio earsmart denials
- Fix mobicore denials
- Note 5 devices correctly identify the model used
- S6 edge can now properly disable touchkeys without borking touch thanks to a new node in the kernel
- Decommonise wifi parameters, and add support for swlan0 for note 5/s6e+

Kernel changes:​
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
- Port some mm features from 3.18
- account for unmovable pages in LMK
- Port ext4 from 3.18
- Port JBD2 from 3.18
- port fusefs from 3.18
- Add p9220 wireless charger firmware
- convert all firmwares to ihex
- remove hacks from kbuild
- Allow hall effect sensor detection to be reversed via config option
- Allow Play Integrity spoofing boot cmdline params to be disabled via option
- initial overlayfs support (may not be complete yet)
- port arm64 features, like hardened user copy
- port bcmhd4359_100 from 8890 for note 5/s6e+ - allows concurrent hotspot and wifi connections
- binder/android updates
- alsa updates
- net updates

## 12.02.2025
- Address denials for fingerprint
- Address denials for DT2W
- Address denials for mobicore
- Address denials for battery on some models
- Address denials for EarSmart IC

## 06.01.2025
- Preliminary support for NA devices

## 05.01.2025
- Sync with LineageOS source
- Update to unofficial ASB 12-2024
- Fix up ADB in recovery - this should allow use of Lineage Recovery now
- Update SEPolicies
- Clean up props
- Add fused location HAL
- Fix up FlipFlap
- Kernel updates
- Add cputime attributes
- Add new locks patches
- RCU patches
- Fix invalid MIF values when boosting GPU
- Remove old mobicore implementations
- Add Available memory to meminfo
- Add denyusb implementation
- Swap to CFQ io sched

## 24.08.2024
- Merge some unofficial ASB patches
- Enable stack protector
- ANT+
- Update SEPolicy to address some denials regarding camera

## 09.08.2024
- Inital release