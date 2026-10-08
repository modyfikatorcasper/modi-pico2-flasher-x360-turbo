# MODI X360 ULTIMATE — service modules

[Polski](FLASHSHIP_PL.md)

**ULTIMATE PREVIEW / IN DEVELOPMENT.** TURBO remains the tested flashing module. ULTIMATE expands it into a target service platform: backup, RGH, CPU Key, Audio/Sonus, glitch-chip programming, LIVE and memory conversions.

| Module | Status | Scope |
|---|---|---|
| TURBO NAND / eMMC | **TESTED** | Tested NAND/eMMC ranges. Binary bytes and timings unchanged. |
| Audio / Sonus | **PREVIEW · HARDWARE VALIDATION PENDING** | Digital ISD2100. MODI RDY = GP22. |
| UART / COM Monitor | **PREVIEW · HARDWARE VALIDATION PENDING** | Live receive, logs and spoken notifications. |
| XeLL CPU Key Assistant | **PREVIEW** | Current LAN panel; target UART/LIVE key capture is in development. |
| HANA / SMBus LIVE Monitor | **PREVIEW · HARDWARE VALIDATION PENDING** | Passive SMBus capture. Full HDMI diagnostics need separate validation. |
| Automatic RGH Assistant | **IN DEVELOPMENT** | Planned single workflow with two backups and final readback. |
| Memory Conversions | **IN DEVELOPMENT** | Planned images for physical memory replacement with 16 MB NAND. |
| Xbox 360 DVD Remarry | **RESEARCH** | Future research module; no remarry function in current firmware. |

**Current state:** one Pico runs one UF2 profile. Audio, MODI Chip Flasher, UART and LIVE are separate builds. LIVE can receive UART and SMBus concurrently; this does not combine all flashing modes. Automatic mode switching in one firmware and one shared application are development goals.

One device, one target service header, one application and successive service modes. Operations do not all run concurrently. The existing NAND GP0–GP5 header does not contain the additional Audio/JTAG/LIVE pins; the shared header must expose them according to the pin map.

[ULTIMATE](ULTIMATE.md) · [Conversions](CONVERSIONS.md) · [Wiring](FLASHSHIP_WIRING.md) · [Pre-final](PRE_FINAL.md) · [Alpha](ALPHA.md)


