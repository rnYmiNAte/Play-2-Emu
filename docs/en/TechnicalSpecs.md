# Play2 Emu Technical Specifications

---

## Emulation Core Architecture
### CPU Emulation
- **Emotion Engine**: Interpreter-based with optional block recompiler (for higher-end devices)
- **IOP**: Cycle-accurate emulation for peripheral support
- **Coprocessors**: VU0/VU1 emulated with vector optimization for rendering

### Rendering Pipeline
- **Backends**:
  - Android: OpenGL ES 2.0+, Vulkan 1.0+
  - iOS: OpenGL ES 2.0+, Metal 1.0+
- **Features**: 4:3 fixed aspect ratio, bilinear filtering, frame sync to NTSC/PAL/SECAM standards

### Disc Image Handling
- **Formats**:
  - `.chd`: Compressed format support via libchdr v0.12
  - `.bin/.cue`: Tracks parsed and streamed sector-by-sector
  - `.iso`: ISO9660/Joliet filesystem support
- **Compression**: Decompression handled via miniz for zlib-based formats

---

## Platform-Specific Optimizations
### Android
- **CPU**: Optimized for ARMv7-A (Cortex A8+) and ARMv8-A (Snapdragon 625+)
- **Memory**: 1 GB minimum allocation with dynamic memory management for older devices

### iOS
- **CPU**: Optimized for ARMv7 (Apple A4+) and ARM64 (Apple A9+)
- **Legacy Support**: Fallback rendering path for iOS 5–8 (OpenGL ES 1.1 compatibility mode)

---

## Third-Party Library Details
| Library         | Purpose                  | License               | Version Used |
|-----------------|--------------------------|-----------------------|--------------|
| libchdr         | CHD format parsing       | BSD 3-Clause          | v0.12        |
| miniz           | Compression/decompression| MIT                   | v2.2.0       |
| Vulkan Headers  | Vulkan rendering support | Apache 2.0            | v1.3.239     |
