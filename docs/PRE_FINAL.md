# MODI X360 ULTIMATE — pre-final / Alpha

[Polski](PRE_FINAL_PL.md) · [ULTIMATE](ULTIMATE.md)

**ULTIMATE PREVIEW / IN DEVELOPMENT — 2026-10-08**

The Stable channel preserves the tested TURBO v0.9.1-beta binaries. The Alpha channel exposes separate preview profiles and their corresponding source. The previous v0.9.1-beta name, files and tag remain preserved.

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

The full local JRunner LIVE preview is excluded from the public package. Alpha contains the MODI-Flashship companion for Audio, MODI Chip Flasher, standalone UART and XeLL LAN; the raw LIVE profile needs the compatible MLIV host from local development. A public updater combining these modes with J-Runner remains to be completed.

Tested TURBO and Setup were not rebuilt. Alpha packages existing profile builds; it is not a new unified firmware. No new hardware test was performed during release preparation.

## 1.0 requirements

Before 1.0: unified firmware and safe mode switching; public host updater; hardware tests for Audio (ID/backup/write/readback/play), JTAG (IDCODE/program/verify), UART and concurrent SMBus; CPU Key and full RGH validation; each conversion combination with full readback and console boot; original photos; mobile/PL/EN QA; source and license compliance. DVD Remarry remains research outside the 1.0 commitment.

[Conversions](CONVERSIONS.md) · [Wiring](FLASHSHIP_WIRING.md) · [Alpha instructions](ALPHA.md)

The SOURCE archive contains only required firmware source and dependency source/notices. Private Setup, JRunner.MODI and MODI application source remains non-public.

