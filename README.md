
---

## 📄 Updated README for `Lineageos-22-for-S6-EGDE-ZEROLTEXX`

**Repository:** `https://github.com/project289/Lineageos-22-for-S6-EGDE-ZEROLTEXX`

```markdown
# LineageOS 22 (Android 15) for Samsung Galaxy S6 Edge (zeroltexx)

![LineageOS](https://img.shields.io/badge/LineageOS-22.1-167C80?style=flat-square&logo=lineageos)
![Android](https://img.shields.io/badge/Android-15-3DDC84?style=flat-square&logo=android)
![Status](https://img.shields.io/badge/Status-Experimental-orange?style=flat-square)

---

## ⚠️ WARNING – READ THIS FIRST
> READ THIS FIRST ELSE YOU GONNA GTE FIRED IF THE ALARM DIDNT WORK
> **This software will void your Samsung KNOX warranty (0x1).**  
> Any damage to your device or data is **YOUR responsibility**.  
> Use at your own risk. No one else is liable.
> IF you point a finger AT ME IMA WHOOP YOUR LITTLE THING INTO MONDAY

This is an **alpha / experimental** build. It is **not a daily driver**.  
Calls and mobile data (RIL) do **not** work. Use this ROM only for testing, learning, and fun.

---

## 📥 Download Status

> 🚧 **DOWNLOAD NOT AVAILABLE YET – ROM IS STILL IN DEVELOPMENT**

The build is currently being synced and tested locally.  
A download link will be added here once the first working build is ready (estimated 1–2 weeks).  
**Do not ask for ETAs.**

---

## 📱 About

**LineageOS 22.1** (based on **Android 15**) for the **Samsung Galaxy S6 Edge (SM-G925F / zeroltexx)**.

Built from source using the Exynos 7420 common tree and kernel from the samsungexynos7420 community.

- **ROM size:** ~800 MB – 1.2 GB (depending on options).
- **Build environment:** Local (WSL2 on Windows) after being banned from Crave.io for using the devspace incorrectly.
- **All source code is available on GitHub** – nothing was lost.

---

## ✅ What Works (probably)

- Booting to home screen
- Touchscreen
- Wi‑Fi (manual DNS may have issues)
- Bluetooth (basic)
- Audio (speaker & headphones)
- Graphics (HWUI)
- ADB / MTP
- Some sensors

---

## ❌ What Does NOT Work (bugs)

- **RIL (Cellular, calls, mobile data)** – completely broken. Wi‑Fi only.
- **Stock camera** – green screen / crash. Use Open Camera from Play Store as a workaround.
- **Always On Display (AOD)** – conflicts with fingerprint sensor. Disable AOD if you need fingerprint.
- **NFC** – random crashes.
- **Power off / restart** – may hang. If stuck, hold Vol‑Down + Power for 10 seconds to force reboot.
- **Fingerprint** – works only when screen is on (not in AOD).
- **Manual DNS** – sometimes fails (e.g., with 1.1.1.1, 8.8.8.8).

If you find more bugs, please open an issue with logs (`adb logcat`, `dmesg`).

---

## 🧪 Build Information

| Item | Details |
|------|---------|
| Android version | 15 (LineageOS 22.1) |
| Device | Samsung Galaxy S6 Edge (zeroltexx) |
| Build date | July 2026 |
| Built by | project289 (13 years old) |
| Build host | Local (WSL2 on Windows) + previously Crave.io |
| Kernel version | 3.10 (Exynos 7420) |
| Status | Experimental / Alpha |

---

## 📥 Installation (once download is available)

1. **Prerequisites** – Unlocked bootloader, latest TWRP for zeroltexx.
2. **Backup** your current ROM.
3. **Wipe** in TWRP: System, Data, Cache, Dalvik/ART cache.
4. **Flash** the ROM zip.
5. **(Optional)** Flash MindTheGapps for Android 15.
6. **Reboot** – first boot may take 5–10 minutes.

---

🙏 Credits & Source Code
Component	Source Repository
Common device tree	samsungexynos7420/android_device_samsung_universal7420-common
Device tree (zeroltexx)	samsungexynos7420/android_device_samsung_zeroltexx
Kernel source (GPLv2)	samsungexynos7420/android_kernel_samsung_universal7420
Vendor blobs	samsungexynos7420/proprietary_vendor_samsung
Patches	samsungexynos7420/7420_patches
Special Thanks
The LineageOS Team – for the incredible OS.

fakemanoan – for his tireless work on Exynos 7420 modern Android ports.

The samsungexynos7420 organization – for keeping this old device alive.

The Android Open Source Project (AOSP).

Crave.io – for providing free cloud build servers (even though I got banned, I appreciate the platform).

All other contributors (Ivan_Meler, Enesuzun2002, Ananjaser1211, etc.).

⚖️ License
This ROM distribution is subject to the GNU General Public License v2 because it contains the Linux kernel.

The kernel source code used in this build can be found in the samsungexynos7420/android_kernel_samsung_universal7420 repository.
If you modify the kernel, you must publish your changes under the GPLv2.

Other parts of the ROM (framework, apps) are under Apache License 2.0 as per LineageOS and AOSP.

📞 Contact / Support
GitHub Issues: Use this repository's issue tracker.

XDA Thread: (coming soon)

Built with patience, caffeine, and the help of the open‑source community.

– project289 (Freewriter27654), age 13


## 🛠️ Build It Yourself (for developers)

If you want to build this ROM yourself, use the manifest from:

👉 **[project289/s6_manifests](https://github.com/project289/s6_manifests)**

IF YOU ALSO EDITED YOU MUST GIVE CREDIT TO RIGHT PATH ONLY GIVE CRedit ME IF YOU EDITED THE FILES THAT 
WERE EDITED BY ME 
THESE ARE THE FILES I HAVE UPDATED


================================================================================
S6 Edge Android 15 Build – File Edits Summary
Project: LineageOS 22.1 (Android 15) for Samsung Galaxy S6 Edge (zeroltexx)
Developer: project289 (Freewriter27654)
Date: July 13, 2026
================================================================================

================================================================================
1. REPOSITORY: project289/android_device_samsung_zeroltexx (lineage-22.1)
================================================================================

File: BoardConfig.mk
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added TARGET_ARCH := arm64
- Added TARGET_ARCH_VARIANT := armv8-a
- Added TARGET_CPU_VARIANT := cortex-a53
- Added TARGET_BOARD_PLATFORM := exynos7420
- Added TARGET_BOOTLOADER_BOARD_NAME := zerolte
- Added BOARD_VENDOR := samsung
- Set TARGET_KERNEL_CONFIG := exynos7420-zerolte_defconfig
- Added TARGET_KERNEL_SOURCE := kernel/samsung/universal7420
- Added BOARD_KERNEL_IMAGE_NAME := Image
- Added TARGET_USES_GRALLOC1 := true
- Added TARGET_USES_HWC2 := true
- Added partition sizes (BOOT, RECOVERY, SYSTEM, USERDATA, CACHE)
- Added include device/samsung/universal7420-common/BoardConfigCommon.mk

File: device.mk
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added $(call inherit-product, device/samsung/universal7420-common/device-common.mk)
- Added PRODUCT_NAME := lineage_zeroltexx
- Added PRODUCT_DEVICE := zeroltexx
- Added PRODUCT_MODEL := SM-G925F
- Added PRODUCT_MANUFACTURER := samsung
- Added PRODUCT_BRAND := samsung
- Added $(call inherit-product, hardware/samsung_slsi/linaro_config/device.mk)
- Added PRODUCT_PACKAGES for graphics HALs (composer, mapper, OMX, libgralloc, libhwc, libexynosutils)

File: AndroidProducts.mk
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Set PRODUCT_MAKEFILES := $(LOCAL_DIR)/lineage_zeroltexx.mk

File: system.prop
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added ro.product.model=SM-G925F
- Added ro.product.name=zeroltexx
- Added ro.product.device=zeroltexx
- Added ro.build.product=zeroltexx
- Added ro.telephony.default_network=9,9
- Added ro.build.version.sdk=35
- Added ro.build.version.codename=REL
- Added ro.build.version.release=15

File: vendorsetup.sh (CREATED)
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Created file with:
  add_lunch_combo lineage_zeroltexx-user
  add_lunch_combo lineage_zeroltexx-userdebug
  add_lunch_combo lineage_zeroltexx-eng

File: lineage_zeroltexx.mk (CREATED)
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Created file with product inheritance and definitions (PRODUCT_NAME, PRODUCT_DEVICE, PRODUCT_MODEL, PRODUCT_MANUFACTURER, PRODUCT_BRAND)

File: Android.mk (if applicable)
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added BSP HAL packages to PRODUCT_PACKAGES (composer, mapper, OMX)


================================================================================
2. REPOSITORY: project289/android_device_samsung_universal7420-common (lineage-22.1)
================================================================================

File: BoardConfigCommon.mk
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added BOARD_VENDOR_SEPOLICY_DIRS += device/samsung/slsi_sepolicy/sepolicy/vendor
- Added TARGET_BOARD_PLATFORM_GPU := mali-t760

File: device-common.mk
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added PRODUCT_PACKAGES for Linaro BSP HALs:
  android.hardware.graphics.composer@2.1-impl
  android.hardware.graphics.mapper@2.0-impl
  android.hardware.media.omx@1.0-impl
  android.hardware.media.omx@1.0-service

File: ramdisk/etc/init.samsungexynos7420.rc
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Changed write /proc/sys/vm/swappiness 100 → 80
- Added write /proc/sys/vm/vfs_cache_pressure 150

File: ramdisk/etc/fstab.samsungexynos7420.zero
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Reduced ZRAM size from 2147483648 (2 GB) to 1610612736 (1.5 GB)


================================================================================
3. REPOSITORY: project289/android_kernel_samsung_universal7420 (lineage-22.1)
================================================================================

File: arch/arm64/configs/exynos7420-zerolte_defconfig
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Disabled CONFIG_KALLSYMS_ALL
- Disabled CONFIG_DEBUG_KERNEL
- Disabled CONFIG_SCHED_DEBUG
- Disabled CONFIG_SCHEDSTATS
- Disabled CONFIG_TIMER_STATS
- Disabled CONFIG_DEBUG_BUGVERBOSE
- Disabled CONFIG_DEBUG_INFO
- Added CONFIG_CGROUP_BPF=y
- Added CONFIG_BPF_SYSCALL=y
- Added CONFIG_USER_NS=y
- Added CONFIG_ARM64=y
- Added CONFIG_ARCH_EXYNOS=y
- Added CONFIG_ARCH_EXYNOS7420=y
- Added CONFIG_SMP=y
- Added CONFIG_HZ=300

File: arch/arm64/mm/proc.S
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Removed stray "#" character at the end of line 193 (assembler error fix)


================================================================================
4. REPOSITORY: project289/s6_manifests (main branch)
================================================================================

File: zeroltexx.xml
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added all missing BSP and sepolicy repos:
  * samsungexynos7420/android_hardware_samsung_slsi-linaro_exynos (lineage-21.0)
  * samsungexynos7420/android_hardware_samsung_slsi-linaro_exynos5 (lineage-21.0)
  * samsungexynos7420/android_hardware_samsung_slsi-linaro_openmax (lineage-21.0)
  * samsungexynos7420/android_hardware_samsung_slsi-linaro_graphics (lineage-21.0)
  * samsungexynos7420/android_hardware_samsung_slsi-linaro_config (lineage-21.0)
  * samsungexynos7420/android_device_samsung_slsi_sepolicy (lineage-21)
- Updated LineageOS/android_hardware_samsung from lineage-22.0 to lineage-22.1
- Updated LineageOS/android_hardware_samsung_slsi_exynos from lineage-22.0 to lineage-19.1
- Updated LineageOS/android_hardware_samsung_slsi_openmax from lineage-22.0 to lineage-19.1
- Updated project289/7420_patches from android15 to lineage-20.0


================================================================================
5. REPOSITORY: project289/7420_patches (lineage-20.0)
================================================================================

Files: Various .patch files
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Applied existing patches (no new patches created):
  * frameworks_base/0001-Revert-fp-always-on-changes.patch
  * frameworks_base/0002-hwui-reset-to-android-13.0.0_r13.patch
  * frameworks_native/0001-Disable-gpu-service.patch
  * frameworks_native/0001-Revert-Remove-obsolete-debug-option.patch
  * frameworks_native/0002-Add-back-pre-S-createEventQueue-function.patch
  * packages_apps_Nfc/Add_sysprop_to_prevent_FW_download.patch
  * packages_modules_NetworkStack/0001-Revert-Enable-parsing-netlink-events-from-kernel-sin.patch
  * system_security/0001-keystore-hackup.patch


================================================================================
6. CLONED (ADDED) REPOSITORIES (Not Edited)
================================================================================

Repo: samsungexynos7420/android_hardware_samsung_slsi-linaro_exynos (lineage-21.0)
Repo: samsungexynos7420/android_hardware_samsung_slsi-linaro_exynos5 (lineage-21.0)
Repo: samsungexynos7420/android_hardware_samsung_slsi-linaro_openmax (lineage-21.0)
Repo: samsungexynos7420/android_hardware_samsung_slsi-linaro_graphics (lineage-21.0)
Repo: samsungexynos7420/android_hardware_samsung_slsi-linaro_config (lineage-21.0)
Repo: samsungexynos7420/android_device_samsung_slsi_sepolicy (lineage-21)


================================================================================
7. PUSHED TO GITHUB
================================================================================

All changes in the following repos have been pushed to the specified branches:

Repo: project289/android_device_samsung_zeroltexx       → branch lineage-22.1 ✅
Repo: project289/android_device_samsung_universal7420-common → branch lineage-22.1 ✅
Repo: project289/android_kernel_samsung_universal7420  → branch lineage-22.1 ✅
Repo: project289/s6_manifests                           → branch main ✅
Repo: project289/7420_patches                           → branch lineage-20.0 ✅


================================================================================
8. LOCAL BUILD ENVIRONMENT (Not Pushed)
================================================================================

File: ~/.wslconfig
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added memory=8GB
- Added swap=16GB
- Added processors=4

File: Environment variables
────────────────────────────────────────────────────────────────────────────────
CHANGES:
- Added export GIT_DISCOVERY_ACROSS_FILESYSTEM=1


================================================================================
9. DOCUMENTATION FILES (CREATED LOCALLY, NOT PUSHED)
================================================================================

File: blueprint.html                    (in Custom os/ and samsung s6 edge dev/)
File: README.md                         (in Custom os/ and samsung s6 edge dev/)
File: build_instructions.txt            (in Custom os/ and samsung s6 edge dev/)
File: local_manifest.xml                (in Custom os/)


================================================================================
10. SUMMARY
================================================================================

Total files edited:               ~15
Total files created:              ~8
Total repositories cloned:        6
Total repositories with changes:  5
Total repositories pushed:        5

All device tree, kernel, manifest, and patch changes are on GitHub.
All BSP and sepolicy repos are cloned and integrated.
The build source is syncing to F:/lineage.

================================================================================
END OF REPORT
================================================================================
```bash
repo init -u https://github.com/project289/s6_manifests.git -b main -m zeroltexx.xml
repo sync -c -j4 --force-sync --no-clone-bundle --no-tags
source build/envsetup.sh
export TARGET_PRODUCT=lineage_zeroltexx
export TARGET_BUILD_VARIANT=userdebug
export TARGET_RELEASE=aosp_current
export TARGET_DEVICE=zeroltexx
make -j4 bacon
