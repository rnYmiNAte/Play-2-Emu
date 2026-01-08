# Play2 Emu Disc Image Conversion Guide
*Last updated: January 8, 2026*

---

## Why Convert Images?
- Reduce file size (`.chd` is up to 70% smaller than `.iso`/`.bin/.cue`)
- Improve compatibility (`.chd` is optimized for emulation)
- Simplify file management (single file vs. multiple `.bin` files)

---

## Tools Needed
| Format Conversion       | Recommended Tool          | Platforms Supported       |
|-------------------------|---------------------------|---------------------------|
| `.bin/.cue` → `.chd`    | `chdman` (from MAME Tools)| Windows, macOS, Linux     |
| `.iso` → `.chd`         | `chdman`                  | Windows, macOS, Linux     |
| Physical Disc → `.iso`  | ImgBurn (Windows) / Disk Utility (macOS) | Windows, macOS |

---

## Step-by-Step Conversion Guides

### Convert `.bin/.cue` or `.iso` to `.chd`
1. **Download MAME Tools**  
   Get the latest version from [MAME’s official site](https://www.mamedev.org/) – extract `chdman.exe` (Windows) or `chdman` (macOS/Linux) to a folder with your disc image.

   ![chdman Setup](assets/conversion_screenshots/chdman_setup.png)

2. **Run Conversion Command**
   - **For `.bin/.cue`**:  
     Open Command Prompt/Terminal, navigate to the folder, and run:  
     ```bash
     chdman createcd -i input.cue -o output.chd
     ```
   - **For `.iso`**:  
     Run:  
     ```bash
     chdman createcd -i input.iso -o output.chd
     ```
3. **Verify the File**  
   Check that `output.chd` appears in the folder – transfer it to your device and load via Play2 Emu.

### Convert Physical PS2 Disc to `.iso`
- **Windows**: Use ImgBurn  
  1. Insert the disc, open ImgBurn → Select "Create image file from disc"  
  2. Choose save path and format (`.iso`) → Click "Start"
- **macOS**: Use Disk Utility  
  1. Insert the disc, open Disk Utility → Select the disc from the sidebar  
  2. Click "File > New Image > Image from [Disc Name]" → Save as `.cdr`, then rename to `.iso`

   ![ISO Conversion](assets/conversion_screenshots/iso_convert.png)

---

## Important Notes
- Only convert discs you own legally
- Avoid compressing images further with ZIP/RAR (emulator can’t read compressed archives)
- Keep original images as backups – converted `.chd` files are not reversible without extra steps
