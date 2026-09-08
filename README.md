# Moonlight Enhanced Plus

**Moonlight Enhanced Plus** is an UNOFFICIAL, community-maintained fork of [Moonlight Android](https://github.com/moonlight-stream/moonlight-android).

⚠️ **Disclaimer:** This project is NOT affiliated with, endorsed by, or supported by NVIDIA Corporation, the official Moonlight project, or its developers. This fork was developed with the extensive assistance of Artificial Intelligence (Google Deepmind Antigravity). Please do not report bugs regarding this fork to the official Moonlight developers.

## 🌟 Features & Changes from Upstream

This fork focuses on enhancing the mobile and tablet streaming experience by replacing static on-screen buttons with a highly customizable floating UI.

### 1. Draggable Floating Bubbles (UI Enhancement)
- Replaced the static keyboard and menu overlay buttons with modern, floating circular "bubbles".
- **Free Dragging:** The bubbles can be dragged anywhere on the screen during your gaming session.
- **Persistent State:** Bubble positions are saved using normalized coordinates, meaning they will stay exactly where you left them across sessions, reboots, and screen rotations.
- **Render-Safe Architecture:** Custom drawable selectors were designed specifically to avoid `SurfaceFlinger` hardware composition crashes when rendering ripple projection masks over video surfaces on 60fps (especially important for environments like Waydroid).

### 2. Live Overlay Customization Panel
When you tap the Menu bubble, a new set of controls allows you to customize the bubbles in real-time without leaving your stream:
- **Opacity Slider:** Adjust the translucency of the bubbles so they don't obscure your gameplay (from 20% to 100%).
- **Size Slider:** Scale the bubbles from a tiny 30dp footprint up to a massive 82dp footprint.
- **Color Picker:** Instantly theme the bubble backgrounds with White, Red, Green, or Blue presets.
- **Reset Layout:** A quick "Reset Controls Layout" button to restore default positions, sizes, and colors.
- **Toggle Visibility:** Quickly hide the Keyboard bubble if you're using a physical controller.

### 3. Legal & Branding Updates
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
