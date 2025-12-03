# Installing Play2 Emu on Android

## 📱 Minimum Requirements
- Android 4.0 – 6.0 (minimum) / 6.0+ recommended
- 1 GB RAM (2 GB recommended)
- CPU: Cortex-A8 → Snapdragon 625 recommended

## 📥 Installation Steps

### **Method 1 — Install APK (Recommended)**
1. Download the latest APK from the Releases page.
2. Enable:
   **Settings → Security → Install Unknown Apps**
3. Open the APK to install it.

### **Method 2 — Install via ADB**
```bash
adb install play2-emu.apk

▶️ First Launch Setup

1. When prompted, select PS2 BIOS file
(You must dump your own BIOS from your console).


2. Add your games:

.iso

.bin/.cue

.chd



3. Play any game from All Games menu.



⚙️ Graphics Configuration

Rendering Mode: Vulkan (recommended)

Aspect Ratio: Locked to 4:3

Lower Internal Resolution if game runs slow


🎮 Controller Setup

Go to Settings → Controller Settings

Customize:

Touchscreen layout

Controller 1 & 2

USB ports

Profiles

Hotkeys



🧩 Troubleshooting

Game running slow?

Switch to Vulkan

Lower resolution

Close background apps


BIOS not detected?

Verify filename:

SCPH10000.bin

SCPH30004.bin

SCPH39001.bin Allows multiple versions.

