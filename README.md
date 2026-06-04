# Lineageos-22-for-S6-EGDE-ZEROLTEXX
LineageOS 22 (Android 15) for Samsung Galaxy S6 Edge (zeroltexx) – built from source by a 13‑year‑old developer. Experimental. Wi‑Fi only.
# LineageOS 22 (Android 15) for Samsung Galaxy S6 Edge (zeroltexx)

![LineageOS](https://img.shields.io/badge/LineageOS-22.1-blue?logo=lineageos)
![Android](https://img.shields.io/badge/Android-15-green?logo=android)
![Status](https://img.shields.io/badge/status-alpha-red)

## ⚠️ Important – Please Read

This is an **alpha / experimental** build. It is **not a daily driver**.  
Calls and mobile data (RIL) do **not** work. Use this ROM only for testing, learning, and fun.

---

## 📱 About

LineageOS 22.1 (based on Android 15) for the **Samsung Galaxy S6 Edge (SM-G925F / zeroltexx)**.  
Built from source using the Exynos 7420 common tree and kernel from the `samsungexynos7420` community.  
**ROM size:** ~800 MB – 1.2 GB (depending on options).  
**Build environment:** Crave.io cloud DevSpace.

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

## ❌ What Does NOT Work (bugs)

- **RIL (Cellular, calls, mobile data)** – completely broken. Wi‑Fi only.
- **Stock camera** – green screen / crash. Use **Open Camera** from Play Store as a workaround.
- **Always On Display (AOD)** – conflicts with fingerprint sensor. Disable AOD if you need fingerprint.
- **NFC** – random crashes.
- **Power off / restart** – may hang. If stuck, hold **Vol‑Down + Power** for 10 seconds to force reboot.
- **Fingerprint** – works only when screen is on (not in AOD).
- **Manual DNS** – sometimes fails (e.g., with 1.1.1.1, 8.8.8.8).

*If you find more bugs, please open an issue with logs (`adb logcat`, `dmesg`).*

---

## 📥 Installation

1. **Prerequisites**
   - Unlocked bootloader
   - Latest **TWRP** for `zeroltexx`

2. **Backup** your current ROM (always do this).

3. **Wipe** in TWRP:
   - System
   - Data
   - Cache
   - Dalvik/ART cache

4. **Flash** the ROM zip.

5. **(Optional)** Flash **MindTheGapps** for Android 15 (or any Gapps package that supports API level 35/Android 15).

6. **Reboot** and wait. First boot may take 5–10 minutes.

---

## 🧪 Build Information

- **Android version:** 15 (LineageOS 22.1)
- **Device:** Samsung Galaxy S6 Edge (zeroltexx)
- **Build date:** June 2026
- **Built by:** [project289](https://github.com/project289) (13 years old)
- **Build host:** Crave.io cloud DevSpace

---

## 🙏 Credits & Source Code

This ROM would not exist without the hard work of the open‑source community.

| Component | Source Repository |
|-----------|-------------------|
| Common device tree | [`samsungexynos7420/android_device_samsung_universal7420-common`](https://github.com/samsungexynos7420/android_device_samsung_universal7420-common) |
| Device tree (zeroltexx) | [`samsungexynos7420/android_device_samsung_zeroltexx`](https://github.com/samsungexynos7420/android_device_samsung_zeroltexx) |
| Kernel source (GPLv2) | [`samsungexynos7420/android_kernel_samsung_universal7420`](https://github.com/samsungexynos7420/android_kernel_samsung_universal7420) |
| Vendor blobs | [`samsungexynos7420/proprietary_vendor_samsung`](https://github.com/samsungexynos7420/proprietary_vendor_samsung) |
| Patches | [`samsungexynos7420/7420_patches`](https://github.com/samsungexynos7420/7420_patches) |

### Special Thanks
Credits cuz used some kernals and divice tree from fakemanoan
- **The LineageOS Team** – for the incredible OS.
- **fakemanoan** – for his tireless work on Exynos 7420 modern Android ports.
- **The `samsungexynos7420` organization** – for keeping this old device alive.
- **The Android Open Source Project (AOSP)**.
- **Crave.io** – for providing free cloud build servers.
- All other contributors (Ivan_Meler, Enesuzun2002, Ananjaser1211, etc.).

---

## ⚖️ License

This ROM distribution is subject to the **GNU General Public License v2** because it contains the Linux kernel.  
The kernel source code used in this build can be found in the [`samsungexynos7420/android_kernel_samsung_universal7420`](https://github.com/samsungexynos7420/android_kernel_samsung_universal7420) repository.  
If you modify the kernel, you **must** publish your changes under the GPLv2.

Other parts of the ROM (framework, apps) are under **Apache License 2.0** as per LineageOS and AOSP.

---

## 📞 Contact / Support

- **XDA thread:** *(link once posted)* for now its not cuz its in devolepment
- **GitHub Issues:** Use the issue tracker of this repository.

---

*Built with patience, caffeine, and the help of the open‑source community.*  
**– project289, age 13**

for now the rom its not published but it would be published after 3days or maybe 1week 
IN DEVOLEPMENT FOR NOW
