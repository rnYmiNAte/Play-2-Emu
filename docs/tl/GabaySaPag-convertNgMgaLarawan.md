# Gabay Sa Pag-convert ng Mga Larawan ng Disc ng Play2 Emu

---

## Bakit Kailangang I-convert ang Mga Larawan?
- Pwedeng bawasan ang laki ng file (ang `.chd` ay hanggang 70% na mas maliit kaysa sa `.iso`/`.bin/.cue`)
- Mas mabuting umaangkop sa emulator (ang `.chd` ay inayos para sa emulasyon)
- Mas madaling pangasiwaan ang mga file (isang file lang kaysa maraming `.bin` file)

---

## Mga Kailangang Gamit
| Pag-convert ng Format    | Inirerekomendang Gamit        | Mga Platformang Maaaring Gamitin |
|--------------------------|--------------------------------|-----------------------------------|
| `.bin/.cue` → `.chd`     | `chdman` (mula sa MAME Tools)  | Windows, macOS, Linux             |
| `.iso` → `.chd`          | `chdman`                       | Windows, macOS, Linux             |
| Pisikal na Disc → `.iso` | ImgBurn (Windows) / Disk Utility (macOS) | Windows, macOS          |

---

## Hakbang-sa-Hakbang na Gabay sa Pag-convert
### I-convert ang `.bin/.cue` o `.iso` patungo sa `.chd`
1. **I-download ang MAME Tools**  
   Kunin ang pinakabagong bersyon mula sa [opisyal na site ng MAME](https://www.mamedev.org/) – i-extract ang `chdman.exe` (Windows) o `chdman` (macOS/Linux) sa isang folder kasama ang iyong larawan ng disc.

2. **Patakbuhin ang Command ng Pag-convert**
   - **Para sa `.bin/.cue`**:  
     Buksan ang Command Prompt/Terminal, pumunta sa folder, at patakbuhin:  
     ```bash
     chdman createcd -i input.cue -o output.chd
     ```
   - **Para sa `.iso`**:  
     Patakbuhin:  
     ```bash
     chdman createcd -i input.iso -o output.chd
     ```
3. **Suriin ang File**  
   Tiyaking lumabas ang `output.chd` sa folder – ilipat ito sa iyong device at buksan gamit ang Play2 Emu.
