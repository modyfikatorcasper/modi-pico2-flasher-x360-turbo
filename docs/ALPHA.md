# MODI X360 ULTIMATE Alpha 1 — 1.0.0-alpha.1

[Polski](ALPHA_PL.md) · [ULTIMATE](ULTIMATE.md)

**ALPHA / PREVIEW · HARDWARE VALIDATION PENDING**

This packages existing builds from 5 October 2026, published on 8 October. It is not a new unified ULTIMATE firmware. Stable preserves the tested TURBO.

## Installation

1. Download and extract the complete Alpha ZIP, then run MODI-Flashship.exe. Windows / .NET Framework 4.8. MODI-Setup.exe remains the stable TURBO installer for your own compatible J-Runner installation.
2. In BOOTSEL flash one profile from the table. Do not copy every UF2 at once. Close the application using COM before starting another tool.
3. Use the selected module wiring diagram. Audio RDY = GP22, GP11 = passive SMB_DATA. 3.3 V logic and common ground.
4. Restore TURBO for NAND/eMMC. Alpha does not change tested NAND/eMMC timings.

| Profile | Host / scope |
|---|---|
| MODI-Pico2-Flasher-X360-TURBO.uf2 | Stable JRunner.MODI; NAND/eMMC |
| MODI-Audio-Sonus-PREVIEW.uf2 | MODI-Flashship → Audio / Sonus; GP12–15, **RDY GP22** |
| MODI-DirtyJTAG-PREVIEW.uf2 | MODI-Flashship → MODI Chip Flasher; GP16–19; xsvftool helper and driver from your own installation |
| MODI-UART-MONITOR-PREVIEW.uf2 | MODI-Flashship → COM / UART; MUAR; GP9 RX |
| MODI-LIVE-UART-HANA-PREVIEW.uf2 | Advanced UART+SMBus profile; requires the local-preview MLIV host, not included in this public ZIP |

The primary MODI-X360-ULTIMATE-UART-ALPHA.uf2 download has identical bytes to MODI-UART-MONITOR-PREVIEW.uf2. It provides UART receive only, not the entire ULTIMATE feature set.


XeLL LAN remains a separate application panel. Automatic RGH, CPU Key through UART/LIVE, memory conversions and DVD Remarry remain in development. Passive SMBus capture is not a full HDMI test.

## Tests and source

Companion offline tests exited with code 0; UF2 structures, ZIP CRC and hashes were checked. This is not a hardware test. Audio, JTAG, UART and SMBus require physical validation. One SOURCE archive contains corresponding source for all five profiles and required dependencies/licenses. It contains no private application source.

[Wiring](FLASHSHIP_WIRING.md) · [Photo credits](PHOTO-CREDITS.md)

