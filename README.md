# Moonlight Enhanced Plus

This fork adds touch-focused session controls and overlay customization on top of Moonlight Android.

> **Unofficial fork notice**
>
> Moonlight Enhanced Plus is not affiliated with, endorsed by, or supported by
> NVIDIA, the Moonlight project, Sunshine, or the original Moonlight maintainers.
>
> Please report fork-specific bugs and feature requests in this repository, not
> to the upstream Moonlight project.

> **AI-assisted development**
>
> This fork was developed with substantial assistance from AI tools, including
> Google DeepMind Antigravity. This is disclosed intentionally and transparently.
> If AI-assisted development is a dealbreaker for you, this project may not be
> a good fit.

## 🌟 Features & Changes from Upstream

### 1. Touch-Focused Controls
- **On-Screen Keyboard Button:** Added a dedicated on-screen button to invoke the software keyboard. This avoids the need to rely on multi-touch gestures that can sometimes conflict with game inputs.
- **On-Screen Session Menu Button:** Added a dedicated button to easily open the Moonlight session settings (to switch monitors, send Ctrl+Alt+Del, or disconnect).
- **Direct Mouse by Default:** Changed the default touch behavior from relative trackpad mode to "Absolute Touch" (direct click), which can make touch-based navigation more intuitive out of the box.

### 2. Floating Customization Panel
The new buttons are implemented as customizable floating overlays:
- **Free Drag-and-Drop:** The Keyboard and Menu bubbles can be dragged anywhere on the screen so they don't obscure your gameplay.
- **Persistent Memory:** Bubble positions are saved automatically using normalized screen coordinates, retaining their location across sessions and screen rotations.
- **Live Customization:** Tapping the Menu bubble opens an interface to customize the overlay in real-time:
  - **Opacity Slider:** Adjust translucency (20% to 100%).
  - **Size Slider:** Scale the bubbles from 30dp up to 82dp.
  - **Color Picker:** Theme the bubbles with White, Red, Green, or Blue presets.
  - **Visibility Toggle:** Hide the Keyboard bubble when using a physical controller.
  - **Reset Layout:** Restore default positions, sizes, and colors.
- **Menu Reordering:** Reordered the session menu to prioritize frequently used options (Switch Monitor and Actions).

### 3. Lightweight UI Architecture
- **Safe Overlay Rendering:** We implemented the UI using simplified drawable selectors instead of complex ripple projection masks. This aims to improve rendering compatibility and reduce clipping anomalies on certain Android distributions, hardware, or environments (like Waydroid) where the GPU compositor may struggle rendering overlays on top of high-framerate hardware-decoded video surfaces.

### 4. Legal & Branding Updates
- App branding and visible name updated to **Moonlight Enhanced Plus**.
- Included a mandatory First-Run Disclaimer Dialog ensuring users understand this is an unofficial fork.
- Added a permanent "About" section in the Android preferences panel.

## 🛠️ Building

Since this repository contains native C/C++ code for decoding, you will need the Android NDK to compile it.

1. Install Android Studio and the Android NDK.
2. Clone the repository and initialize submodules:
   ```bash
   git clone https://github.com/BetaDev55/moonlight-enhanced-plus.git
   cd moonlight-enhanced-plus
   git submodule update --init --recursive
   ```
3. Build the APK using Gradle:
   ```bash
   ./gradlew assembleDebug
   ```
   *The resulting APK will be located at:* `app/build/outputs/apk/nonRoot/debug/app-nonRoot-debug.apk`

---

## 📜 Upstream Attribution
This project is built upon [Moonlight Android](https://github.com/moonlight-stream/moonlight-android).
For documentation, server setup, and core functionality, refer to the upstream project.

**Original Moonlight Authors:**
* Cameron Gutman
* Diego Waxemberg
* Aaron Neyer
* Andrew Hennessy

Moonlight is open source software released under the GPLv3 license.
