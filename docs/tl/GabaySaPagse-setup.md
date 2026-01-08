# Gabay Sa Pagse-setup ng Play2 Emu

---

## Para sa Android Device
### Hakbang 1: Payagan ang Mga App na Hindi Mula sa Google Play
- Pumunta sa **Mga Setting > Seguridad > Mga Pinagmumulan na Hindi Kilala** at i-toggle ito patungo sa "Bukas" (para sa Android 4.0 hanggang 7.0)
- Para sa Android 8.0 pataas, payagan ang pag-install mula sa app na ginamit mong i-download ang APK file

### Hakbang 2: Paglalagay ng BIOS File
- Kailangang BIOS file: `ps2_bios.bin` (pwede ring `scph10000.bin`, `scph39001.bin`, at iba pa)
- Ilagay ang file sa alinman sa mga sumusunod na lokasyon:
  - `/Internal Storage/Play2Emu/bios/`
  - `/SD Card/Play2Emu/bios/`
- Susuriin ng app ang mga direktoryong ito sa unang pagbukas

---

## Para sa iOS Device
### Hakbang 1: Pag-install Gamit ang Xcode (para sa mga Developer)
1. Ikonekta ang iyong iOS device sa iyong Mac
2. Buksan ang `ios/Play2Emu.xcodeproj` gamit ang Xcode
3. Piliin ang iyong device bilang target at pindutin ang "Run"

### Hakbang 2: Paglalagay ng BIOS File
- Gamitin ang **File Picker** sa app para i-import ang iyong BIOS file
- Maimamahagi ang file sa sandbox directory ng app: `Documents/bios/`
