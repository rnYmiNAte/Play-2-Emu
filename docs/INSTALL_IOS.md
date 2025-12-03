# **📄 INSTALL_IOS.md**

```markdown
# Installing Play2 Emu on iOS

## 📱 Minimum Requirements
- iOS 5 – 9 (minimum) / iOS 9+ recommended
- CPU: Apple A4 → Apple A9 recommended
- 1 GB RAM (2 GB recommended)

## 📥 Installation Methods

### **Method 1 — AltStore (Recommended)**
1. Install AltStore on your iOS device.
2. Download the `.ipa` from the GitHub Releases page.
3. Open the `.ipa` with AltStore.
4. AltStore will sign and install the app.

### **Method 2 — Sideloadly**
1. Download the `.ipa`.
2. Open Sideloadly on your PC.
3. Drag & drop the `.ipa` into Sideloadly.
4. Connect your device and install.

### **Method 3 — Xcode (Developer Mode)**
1. Clone repository:
```bash
git clone https://github.com/ampplay/play2-emu.git

2. Open Play2.xcodeproj or workspace in Xcode.


3. Select your device.


4. Click Run.



▶️ Setup After Install

1. Provide PS2 BIOS from your hardware.


2. Add games using:

iTunes File Sharing

Files App → Save to Play2 Emu

AirDrop




⚙️ Recommended Settings

Rendering Mode: OpenGL or Metal (device-dependent)

Max resolution: Native

Audio synchronization: Enabled


🧩 Troubleshooting

App crashes immediately?

Sign the .ipa with a valid certificate.

Game list empty?

Ensure files are in:

On My iPhone → Play2 Emu → games/

BIOS not showing?

Verify correct filename and extension.