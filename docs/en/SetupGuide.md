# Play2 Emu Setup Guide

---

## Android Setup
### Step 1: Enable Unknown Sources (for APK installs)
- Go to **Settings > Security > Unknown Sources** and toggle it on (Android 4.0–7.0)
- For Android 8.0+, allow installation from the specific app used to download the APK

### Step 2: BIOS Installation
- Required BIOS file name: `ps2_bios.bin` (or `scph10000.bin`, `scph39001.bin`, etc.)
- Place the file in one of these paths:
  - `/Internal Storage/Play2Emu/bios/`
  - `/SD Card/Play2Emu/bios/`
- The app will scan these directories on first launch

---

## iOS Setup
### Step 1: Install via Xcode (for developers)
1. Connect your iOS device to your Mac
2. Open `ios/Play2Emu.xcodeproj` in Xcode
3. Select your device as the build target and click "Run"

### Step 2: BIOS Installation
- Use the **File Picker** in the app to import your BIOS file
- The file will be stored in the app’s sandbox directory: `Documents/bios/`
