# Play2 Emu
A lightweight PlayStation 2 emulator for Android and iOS, developed by **ampplay**.

---

## Key Features
- Supports disc image formats: `.chd`, `.bin/.cue`, `.iso`
- Rendering backends: OpenGL, Vulkan (Android) | OpenGL ES, Metal (iOS)
- Fixed 4:3 aspect ratio output
- Syncs to 29.97 fps (NTSC) / 25 fps (PAL/SECAM)

---

## System Requirements

### Android
- **Minimum**: Android 4.0–6.0, Cortex A8-equivalent CPU, 1 GB RAM
- **Recommended**: Android 6.0+, Snapdragon 625-equivalent CPU, 2 GB RAM

### iOS
- **Minimum**: iOS 5–9, Apple A4-equivalent CPU, 1 GB RAM
- **Recommended**: iOS 9+, Apple A9-equivalent CPU, 2 GB RAM

---

## Setup Guide
1. **Install the App**
   - Android: Download APK from [Releases](https://github.com/ampplay/Play2-Emu/releases) or Google Play (coming soon)
   - iOS: Install via Xcode or TestFlight (coming soon)
   
2. **BIOS Setup**
   - Place a valid PS2 BIOS file in your device’s storage (see [SetupGuide.md](./docs/en/SetupGuide.md) for paths)
   - The emulator will auto-detect BIOS files on first launch

3. **Load a Game**
   - Use the built-in file picker to select your `.chd`, `.bin/.cue`, or `.iso` file
   - Tap the game icon to start emulation

---

## Documentation
- Full User Guide: [./docs/en/UserGuide.md](./docs/en/UserGuide.md)
- Compatibility List: [./docs/en/CompatibilityList.md](./docs/en/CompatibilityList.md)
- Contributing: [./docs/CONTRIBUTING.md](./docs/CONTRIBUTING.md)

---

## License
This project is licensed under the **GNU General Public License v3.0** - see [LICENSE](./LICENSE) for details.

Third-party libraries are licensed under their respective terms (see [docs/en/TechnicalSpecs.md](./docs/en/TechnicalSpecs.md) for details).

---

## Disclaimer
Play2 Emu is not affiliated with Sony Interactive Entertainment. Users must own a physical copy of any game they emulate and comply with local copyright laws.
