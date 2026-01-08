# Play2 Emu Settings Quick-Reference Cheat Sheet

---

## **Performance Issues? Use These Settings**
| Problem                  | Recommended Adjustment                                  | Location                  |
|--------------------------|---------------------------------------------------------|---------------------------|
| Low frame rate           | Switch to **OpenGL/OpenGL ES** backend                  | Settings > Rendering      |
| Game freezes             | Reduce **Audio Buffer Size** to "Small"                 | Settings > Audio          |
| Slow loading times       | Move game files to **internal storage**                 | Device settings > Storage |
| PAL games stutter        | Set **Frame Rate** to "25 fps (PAL/SECAM)"              | Settings > Display        |

---

## **Display Issues? Use These Settings**
| Problem                  | Recommended Adjustment                                  | Location                  |
|--------------------------|---------------------------------------------------------|---------------------------|
| Stretched image          | Enable **Force 4:3 Aspect Ratio**                       | Settings > Display        |
| Blurry textures          | Enable **Bilinear Filtering**                           | Settings > Rendering      |
| Black screen on boot     | Toggle **Skip BIOS Splash Screen** off                  | Settings > System         |
| Screen tearing           | Enable **VSync**                                         | Settings > Rendering      |

---

## **Audio Issues? Use These Settings**
| Problem                  | Recommended Adjustment                                  | Location                  |
|--------------------------|---------------------------------------------------------|---------------------------|
| No sound                 | Enable **Audio Output** and check device volume         | Settings > Audio          |
| Audio stutters           | Set **Audio Buffer Size** to "Large"                    | Settings > Audio          |
| Audio out of sync        | Enable **Audio Sync to Frame Rate**                     | Settings > Audio          |

---

## **Legacy Device Tweaks**
| Device Type              | Best Settings Combination                               |
|--------------------------|---------------------------------------------------------|
| Android 4.0–5.0 (Cortex A8) | OpenGL ES backend + Disable texture filtering + Small buffer | All sections above |
| iOS 5–8 (Apple A4/A5)    | OpenGL ES backend + Force 4:3 + 25/29.97 fps lock      | All sections above |
| Android 5.0–6.0 (Snapdragon 400) | OpenGL ES backend + Medium buffer + PAL/NTSC sync | All sections above |

---

## **Quick Setup for New Users**
1. Go to **Settings > System** → Select BIOS file
2. Go to **Settings > Rendering** → Choose backend matching your device
3. Go to **Settings > Display** → Enable Force 4:3
4. Go to **Settings > Audio** → Set buffer size to "Medium"
