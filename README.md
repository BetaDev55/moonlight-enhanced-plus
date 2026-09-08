# Moonlight Enhanced Plus

**Moonlight Enhanced Plus** is an UNOFFICIAL, community-maintained fork of [Moonlight Android](https://github.com/moonlight-stream/moonlight-android).

⚠️ **Disclaimer:** This project is NOT affiliated with, endorsed by, or supported by NVIDIA Corporation, the official Moonlight project, or its developers. This fork was developed with the extensive assistance of Artificial Intelligence (Google Deepmind Antigravity). Please do not report bugs regarding this fork to the official Moonlight developers.

## 🌟 Features & Changes from Upstream

This fork introduces completely new ways to interact with your streaming session, focusing on touchscreen accessibility and customization.

### 1. Core New Features
- **On-Screen Keyboard Button:** Added a dedicated on-screen button to instantly summon the software keyboard during a game. In original Moonlight, invoking the keyboard relies on complex gestures (like a three-finger tap) that often fail or conflict with game inputs.
- **On-Screen Session Menu Button:** Added a dedicated button to easily open the Moonlight session settings (to switch monitors, send Ctrl+Alt+Del, or disconnect) without relying on the Android "Back" gesture.
- **Direct Mouse by Default:** Changed the default touch behavior from relative trackpad mode to "Absolute Touch" (direct click), making touch-based navigation in desktop environments much more intuitive right out of the box.

### 2. Quality of Life (QOL) & Customization
Instead of making these new buttons static, we implemented them as highly advanced **Floating Bubbles**:
- **Free Drag-and-Drop:** The Keyboard and Menu bubbles can be dragged anywhere on the screen so they never block crucial game UI.
- **Persistent Memory:** Bubble positions are automatically saved. They will stay exactly where you left them across sessions, reboots, and screen rotations.
- **Live Customization Panel:** Tapping the Menu bubble opens a new interface that lets you customize the bubbles in real-time:
  - **Opacity Slider:** Adjust the translucency (20% to 100%) so they blend seamlessly into your game.
  - **Size Slider:** Scale the bubbles from 30dp up to 82dp.
  - **Color Picker:** Theme the bubbles with White, Red, Green, or Blue presets.
  - **Visibility Toggle:** Easily hide the Keyboard bubble if you're using a physical controller.
  - **Reset Layout:** Instantly restore default positions, sizes, and colors.
- **Menu Reordering:** Reordered the session menu so that the most frequently used options (Switch Monitor and Actions) are prioritized at the top.

### 3. Stability & Architecture Fixes
- **Render-Safe UI:** Designed custom drawable selectors specifically to avoid Android `SurfaceFlinger` hardware composition crashes. This guarantees 60fps stability without visual artifacts or "clipping" bugs when rendering the floating UI over the video decoder surface (especially critical for environments like Waydroid).

### 4. Legal & Branding Updates
- App renamed internally and externally to **Moonlight Enhanced Plus**.
- Included a mandatory First-Run Disclaimer Dialog ensuring users understand this is an AI-assisted community fork.
- Added a permanent "About" section in the Android preferences panel.

---

## Building
1. Install Android Studio and the Android NDK
2. Run `git submodule update --init --recursive`
3. Build the APK using Android Studio or `./gradlew assembleDebug`

---
*Below is the original README from the upstream Moonlight project for reference:*

# Moonlight Android (Original)

[![Translation Status](https://hosted.weblate.org/widgets/moonlight/-/moonlight-android/svg-badge.svg)](https://hosted.weblate.org/projects/moonlight/moonlight-android/)

[Moonlight for Android](https://moonlight-stream.org) is an open source client for NVIDIA GameStream and [Sunshine](https://github.com/LizardByte/Sunshine).

Moonlight for Android will allow you to stream your full collection of games from your Windows PC to your Android device,
whether in your own home or over the internet.

Moonlight also has a [PC client](https://github.com/moonlight-stream/moonlight-qt) and [iOS/tvOS client](https://github.com/moonlight-stream/moonlight-ios).

You can follow development on our [Discord server](https://moonlight-stream.org/discord) and help translate Moonlight into your language on [Weblate](https://hosted.weblate.org/projects/moonlight/moonlight-android/).

## Authors (Original)

* [Cameron Gutman](https://github.com/cgutman)  
* [Diego Waxemberg](https://github.com/dwaxemberg)  
* [Aaron Neyer](https://github.com/Aaronneyer)  
* [Andrew Hennessy](https://github.com/yetanothername)

Moonlight is the work of students at [Case Western](http://case.edu) and was
started as a project at [MHacks](http://mhacks.org).
