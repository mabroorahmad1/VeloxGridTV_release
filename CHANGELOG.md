# Changelog — VeloxGrid TV

All notable updates and releases for VeloxGrid TV will be documented in this file.

---

## [1.0.0] - 2026-09-17

### Added
* **Google TV / Monet Theme:** Custom dark slate theme (`#0F1117`) with 16dp rounded squircle components.
* **White Outline & Frosted Glass Selector:** Responsive focus engine with 1.1x scaling and 2dp borders.
* **Top Header & Quick Nav:** Pinned brand title, digital TextClock, and interactive Wi-Fi / Bluetooth status shortcuts.
* **Google Play Store Shortcut:** Quick-access chip directly under the top navigation on the Home tab.
* **Favourites Row with Custom Reordering:** Add, remove, and reorder favourite applications directly with D-pad controls.
* **All Apps Drawer:** 5-column grid layout for installed apps and games.
* **Context Engine:** Custom modal for application management (Move, App Info, Remove).
* **Accessibility Zoom Engine:** Dynamic 100% to 200% global UI scaling without clipping or coordinate misalignment.
* **Boot Capture:** Integrated `BOOT_COMPLETED` broadcast receiver for direct startup on power-on.

### Optimized
* **Memory Pruning:** Removed `TvContractCompat` channel recommendation queries, bringing idle RAM usage below 50 MB.
* **Aggressive Bitmap Downsampling:** Downsampled image requests to matching DP-to-pixel targets on low-end chipsets.
* **Render Loop Stability:** Ensured 60 FPS hardware-accelerated scrolling on 1GB RAM Android 9 boxes.
