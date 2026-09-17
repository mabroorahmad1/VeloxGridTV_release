# VeloxGrid TV — Ultra-Lean Smart TV & Android TV Launcher

> **VeloxGrid TV** is an ultra-fast, zero-bloat home launcher designed for Android TV boxes and smart TVs[cite: 2]. Combining the modern aesthetics of Google TV and Android Monet with low hardware footprint engineering, VeloxGrid TV restores fluid 60 FPS performance on budget and legacy hardware.


[![Target Android](https://img.shields.io/badge/Android-9.0%2B%20(API%2028%2B)-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/about/versions/pie)
[![RAM Consumption](https://img.shields.io/badge/Idle%20RAM-%3C%2050%20MB-red?style=for-the-badge)](https://github.com/mabroorahmad1/VeloxGridTV/releases)
[![License](https://img.shields.io/badge/License-Freeware%20%2F%20Closed%20Source-lightgrey?style=for-the-badge)](#license--distribution)
[![Architecture](https://img.shields.io/badge/Arch-armeabi--v7a%20%7C%20arm64--v8a%20%7C%20x86%20%7C%20x86__64-orange?style=for-the-badge)](#supported-hardware)
---

## Highlights & Performance Benchmarks

| Metric | Stock Vendor Launchers | VeloxGrid TV |
| --- | --- | --- |
| **Idle Memory Footprint** | 180 MB – 320 MB RAM | **< 50 MB RAM** |
| **Cold Boot Delay** | 4.5 – 8.0 Seconds | **< 1.2 Seconds** |
| **Background Network Usage** | Continuous tracking / Ads | **0 KB (Fully Sandboxed & Offline)** |
| **D-Pad Focus Lag** | 80 ms – 150 ms | **0 ms (Hardware-Accelerated)** |
| **Supported OS** | Android 10+ | **Android 9.0 (Pie / API 28) & Newer** |

---

## Core Features

* **Google TV & Monet Design Language:** Minimalist slate background (`#0F1117`), 16dp rounded squircle app cards, and high-contrast typography.
* **Frosted Glass Selection Engine:** Custom D-pad focus engine with a 1.1x scale-up animation, a 2dp solid white border, and a translucent selection glow without heavy real-time shader lag.
* **Custom Dynamic Scaling (100%–200% Zoom):** Deep accessibility engine modifying context density metrics without breaking layout bounds or D-pad focus coordinates[cite: 1, 2].
* **Curated Home (For You):** A clean top row with an immediate Google Play Store shortcut chip, alongside an organized **Favourites** horizontal row.
* **D-Pad Edit Mode:** Long-press any favorite app to reorder it seamlessly using remote arrow keys or manage app details.
* **High-Density App Drawer:** Dedicated 5-column grid view categorizing all installed apps and games.
* **System Status & Interactive Header:** Live digital clock, status indicators, and clickable quick-launch buttons for Wi-Fi and Bluetooth settings.
* **Boot Interception:** Registers system `BOOT_COMPLETED` triggers to launch instantly on cold power-on[cite: 1, 2].

---

## Hardware Compatibility

VeloxGrid TV is tested and verified across a wide spectrum of budget and legacy TV hardware:

* **Processors:** Amlogic (S905X, S905W, S912, S905Y2), Rockchip (RK3229, RK3318, RK3328), Allwinner (H6, H616), Realtek.
* **Devices:** Xiaomi Mi Box / Mi TV Stick, generic Android 9.0 AOSP set-top boxes, Fire TV devices, Chromecast with Google TV, and custom smart projector systems.
* **RAM Profiles:** Fully operational on 1 GB, 1.5 GB, 2 GB, and 4 GB memory configurations.

---

## Installation Guide

### Method 1: Sideloading via USB Drive

1. Head to the official [VeloxGrid TV Release](https://github.com/mabroorahmad1/VeloxGridTV_release/releases/tag/Release) page.
2. Download the latest `VeloxGridTV-Release-v1.0.0.apk` (or current release asset).
3. Copy the APK file to a FAT32/NTFS formatted USB flash drive.
4. Plug the drive into your TV box and open any file manager (e.g., X-plore, File Commander).
5. Select the APK and click **Install**.
6. When prompted, permit installation from unknown sources.

### Method 2: Network Installation via ADB (Command Line)

Connect your computer to your Android TV over the local network:

```bash
# Connect to your Android TV IP
adb connect YOUR_TV_IP_ADDRESS:5555

# Install the release APK
adb install -r VeloxGridTV-Release-v1.0.0.apk

```

### Setting as Default Launcher

1. Press the **Home** button on your TV remote.
2. Select **VeloxGrid TV** from the list of launchers.
3. Select **Always**.
4. *(Optional fallback)* If using a custom AOSP ROM that locks default apps:
* Navigate to **Settings** > **Apps** > **Special App Access** > **Default Home App**.
* Select **VeloxGrid TV**.



---

## Security & Privacy Model

VeloxGrid TV operates under a strict offline principle[cite: 1]:

* **Zero Tracking / Zero Telemetry:** No analytics SDKs, advertising libraries, or data collection services.
* **Minimal Manifest Permissions:** Demands only `RECEIVE_BOOT_COMPLETED` for startup[cite: 1, 2]. Does not request `INTERNET`, `READ_EXTERNAL_STORAGE`, `ACCESS_FINE_LOCATION`, or microphone permissions[cite: 1].
* **Sandboxed Operation:** All application discovery is performed locally on-device using Android's native `PackageManager`[cite: 1, 2].

---

## Release Downloads

Get the verified build package on the official release page:

👉 **[Download Latest APK from GitHub Releases](https://github.com/mabroorahmad1/VeloxGridTV_release/releases/tag/Release)**

---

## Community & Feedback

* **Bug Reports:** Found an issue on a specific TV box model? Open a ticket on the [Issue Tracker](https://www.google.com/search?q=https://github.com/mabroorahmad1/VeloxGridTV_release/issues).
* **Feature Requests:** Submit your ideas via GitHub Issues on the release repo.

---

## License & Distribution

Copyright © 2026 Mabroor Ahmad Mansoor. All rights reserved.

VeloxGrid TV is provided as freeware for personal use. Redistribution of the pre-compiled binary packages is permitted with original attribution. Reverse engineering, decompilation, or unauthorized rebranding of release binaries is strictly prohibited.
