# Play2 Emu Troubleshooting Guide
*Last updated: January 8, 2026*

---

## Table of Contents
1. [BIOS & Setup Issues](#bios-setup-issues)
2. [Game Loading & Format Issues](#game-loading-issues)
3. [Performance & Frame Rate Issues](#performance-issues)
4. [Rendering & Display Issues](#rendering-issues)
5. [Audio Issues](#audio-issues)
6. [Platform-Specific Issues](#platform-issues)

---

### <a name="bios-setup-issues"></a>1. BIOS & Setup Issues
#### Issue: "Invalid BIOS File" Error
- **Symptom**: App shows error and exits when loading BIOS
- **Possible Causes**:
  - BIOS file is corrupted or not a valid PS2 BIOS
  - File is not placed in the correct directory
- **Fixes**:
  1. Verify BIOS authenticity (must own original PS2 console to legally use BIOS)
  2. Re-download or transfer the file to ensure it’s not corrupted
  3. Confirm path matches [SetupGuide.md](./SetupGuide.md) requirements

![BIOS Error Example](assets/troubleshooting_images/bios_error_screen.png)

#### Issue: App Crashes on Launch (Android)
- **Symptom**: App closes immediately after opening
- **Fixes**:
  - Clear app cache: **Settings > Apps > Play2 Emu > Storage > Clear Cache**
  - Ensure device runs Android 4.0 or higher
  - For Android 4.0–5.0: Disable Vulkan rendering in app settings (if previously enabled)

---

### <a name="game-loading-issues"></a>2. Game Loading & Format Issues
#### Issue: ".bin/.cue File Fails to Load"
- **Symptom**: App shows "Disc Image Not Found" even when files are present
- **Possible Causes**:
  - `.cue` file references incorrect `.bin` filename/path
  - Multiple `.bin` files are missing or misnamed
- **Fixes**:
  1. Open the `.cue` file in a text editor and verify file paths match
  2. Ensure all `.bin` files are in the same directory as the `.cue` file
  3. Convert to `.chd` format for better compatibility (use tools like `chdman`)

#### Issue: ".iso File is Not Recognized"
- **Fixes**:
  - Ensure the ISO is a valid PS2 data disc (not a video/data CD)
  - Check that the file size is at least 500 MB (most PS2 games are larger)

---

### <a name="performance-issues"></a>3. Performance & Frame Rate Issues
#### Issue: Low Frame Rate or Slowdowns
- **Fixes**:
  1. Adjust render settings (see image below):
     - Switch to OpenGL/OpenGL ES backend (less demanding than Vulkan/Metal)
     - Disable "Texture Filtering" or "Enhanced Resolution"
  2. Close background apps consuming CPU/RAM
  3. For PAL games: Ensure frame rate is set to 25 fps (not 29.97 fps)

![Render Settings Example](assets/troubleshooting_images/render_settings.png)

#### Issue: Game Freezes Randomly
- **Possible Causes**:
  - Insufficient RAM (less than 1 GB minimum)
  - Corrupted disc image
- **Fixes**:
  1. Restart the app and reload the game
  2. Check disc image integrity (re-download or re-convert if needed)
  3. On Android: Move app to internal storage (SD cards may be slower)

---

### <a name="rendering-issues"></a>4. Rendering & Display Issues
#### Issue: Stretched or Wrong Aspect Ratio
- **Symptom**: Game looks distorted (not 4:3)
- **Fix**:
  - Go to **Settings > Display > Aspect Ratio** and select "Force 4:3"
  - Ensure device display scaling is set to default

#### Issue: Black Screen After Loading Game
- **Fixes**:
  1. Wait 30–60 seconds (some games take time to boot)
  2. Switch rendering backends and restart the game
  3. Verify BIOS is compatible with the game region (NTSC/PAL)

---

### <a name="audio-issues"></a>5. Audio Issues
#### Issue: No Sound or Audio Stutters
- **Fixes**:
  1. Check device volume and app audio permissions
  2. In settings, reduce "Audio Buffer Size" (may fix stutters)
  3. For NTSC games: Ensure audio sync is set to 29.97 fps

---

### <a name="platform-issues"></a>6. Platform-Specific Issues
#### Android: "Storage Permission Denied"
- **Fixes**:
  - Go to **Settings > Apps > Play2 Emu > Permissions > Storage** and enable access
  - For Android 10+: Use the "Scoped Storage" option in app settings to select game directory

#### iOS: Game Won’t Install on iOS 5–8
- **Fix**:
  - Use Xcode 9 or older to build the app (newer Xcode versions don’t support legacy iOS)
  - Install via iTunes file sharing for iOS 5–6

---

## Still Having Issues?
- Check the [Compatibility List](./CompatibilityList.md) to see if your game has known issues
- Report problems on the [GitHub Issues Page](https://github.com/ampplay/Play2-Emu/issues) and include:
  - Device model and OS version
  - Game title and format
  - Screenshot of the error (if applicable)
