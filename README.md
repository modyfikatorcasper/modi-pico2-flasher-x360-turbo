# MODI Pico 2 Flasher X360 TURBO

**Fast low-cost Xbox 360 NAND & eMMC flasher for RP2350 / Pico 2 with J-Runner integration.**  
Corona, Trinity and Fat wiring diagrams. One MODI header. One SPI workflow. Stable TURBO.

[🇵🇱 Polski](README_PL.md) · **🇬🇧 English**

[![Open MODI Pico 2 Flasher X360 TURBO](assets/buttons/open-modi-flasher.svg)](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/)


## FLASHSHIP / ULTIMATE — agreements and lab notes

**FLASHSHIP = RP2350 hardware · X360 ULTIMATE = the complete target system · TURBO = NAND/eMMC module.**

**ONE DEVICE. ONE HEADER. ONE SOFTWARE.** Current Alpha uses separate UF2 profiles; unified automation remains a development goal.

[Project agreements](docs/PROJECT-AGREEMENTS.md) · [DEVLOG / LAB NOTES](docs/DEVLOG.md) · [Website journal](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/#devlog)

## Project identity

**Kacper Lewandowski — `modyfikatorcasper` on GitHub, also known as Modyfikator89, Modyfikator Kacper and Modi.**  
MODI Diagnostic Lab is the common name used for these technical projects.

**Kacper Lewandowski — GitHub: `modyfikatorcasper`, znany również jako Modyfikator89, Modyfikator Kacper i Modi.**  
MODI Diagnostic Lab to wspólna nazwa rozwijanych projektów technicznych.

## Download

**[DOWNLOAD UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO.uf2)**  
[DOWNLOAD COMPLETE PACKAGE](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip)  
[OPEN PROJECT PAGE](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/) · [MANUAL](docs/INSTALL.md) · [WIRING](docs/WIRING.md)

![MODI Pico 2 Flasher X360 TURBO](assets/logo/modi-turbo.png)

## Xbox 360 flasher built for speed and service

**MODI Pico 2 Flasher X360 TURBO** is an independent Xbox 360 NAND and eMMC service flasher built around inexpensive **RP2350 / Pico 2-class hardware**.

It is designed for console repair, NAND backup, flash recovery and RGH service work while keeping the user workflow simple. Flash the UF2, run the installation package, connect the flasher and use the MODI integration with J-Runner.

### Tested hardware results

| Memory / tested range | READ | WRITE |
|---|---:|---:|
| 16 MB NAND | ~19 s | ~24 s |
| Jasper Big Block, tested 64 MiB + spare | 76.890–76.955 s | 90.171 s |
| Corona eMMC, tested 48 MiB | 56.198–57.792 s | 48.310 s |

Measured on tested hardware. Actual performance can vary with motherboard revision, wiring, USB host and system configuration.

We currently describe MODI as **one of the fastest low-cost Xbox 360 flashing solutions we have tested**. A broader public comparison would be needed before making an absolute worldwide speed claim.

## One header. One SPI workflow.

The MODI-side wiring stays consistent across the supported Xbox 360 service diagrams.

**GP0 = SPI_MISO**  
**GP1 = SPI_SS_N**  
**GP2 = SPI_CLK**  
**GP3 = SPI_MOSI**  
**GP4 = SMC_DBG_EN**  
**GP5 = SMC_RST_XDK_N**  
**GND = GND**

On our seven-position RP2350-Plus header, moving down from USB:

**orange GP0 → brown GP1 → yellow GND → red GP2 → black GP3 → blue GP4 → green GP5**

Wiring diagrams:

- [Corona](assets/wiring/wiring-corona-rp2350-plus.png)
- [Trinity](assets/wiring/wiring-trinity-rp2350-plus.png)
- [Falcon / Fat](assets/wiring/wiring-falcon-rp2350-plus.png)
- [Full wiring manual](docs/WIRING.md)

Always verify the motherboard revision and pads before connecting hardware.

## Quick start

1. Download `MODI-Pico2-Flasher-X360-TURBO.uf2` or the complete release package.
2. Put the Pico 2 / RP2350 board into **BOOTSEL** mode and copy the UF2.
3. Wire the flasher using the correct motherboard diagram.
4. Run **MODI-Setup.exe**.
5. Select or detect the supported **J-Runner with Extras 3.4.0.7** installation.
6. Click **Install MODI TURBO**. The original J-Runner remains unchanged.
7. Connect MODI Pico 2 Flasher X360 TURBO.
8. Use **READ → BACKUP → COMPARE/VERIFY** before any write operation.

Detailed guide: [Installation EN](docs/INSTALL.md) · [Instalacja PL](docs/INSTALL_PL.md)

## Why MODI?

Early Xbox 360 NAND workflows could take tens of minutes on older interfaces such as LPT. USB programmers improved that dramatically. Modern low-cost microcontrollers make another step possible.

MODI was built around a simple goal: **make fast Xbox 360 flash service accessible with cheap hardware without turning the setup into a developer project.**

The project is focused on:

- Xbox 360 NAND service
- Corona eMMC service
- Jasper Big Block
- RGH repair workflows
- NAND backup and recovery
- J-Runner integration
- Right to Repair

## Low-cost hardware

The project targets inexpensive RP2350 / Pico 2-class boards. The core development board can often be found for roughly **USD $5–6**, depending on region and supplier. This price refers to the board only and excludes wiring, adapters and shipping.

## THE NEXT STEP: MODI X360 ULTIMATE

**All-in-One Xbox 360 Service Tool · ULTIMATE PREVIEW / IN DEVELOPMENT**

![MODI X360 ULTIMATE](assets/logo/modi-x360-ultimate-transparent.png)

TURBO remains the tested flashing module. ULTIMATE expands it into a target service platform: backup, RGH, CPU Key, Audio/Sonus, glitch-chip programming, LIVE and memory conversions.

**ONE DEVICE. ONE HEADER. ONE SOFTWARE. FULL XBOX 360 SERVICE WORKFLOW.**

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

[ULTIMATE](docs/ULTIMATE.md) · [Conversions](docs/CONVERSIONS.md) · [Alpha](docs/ALPHA.md) · [Wiring](docs/FLASHSHIP_WIRING.md)

**MODI Audio RDY = GP22; GP11 = passive SMB_DATA.**

Stable: tested TURBO baseline. Alpha: new modules requiring hardware validation.


## Credits

This project builds on years of Xbox 360 service and homebrew work.

Special thanks to **Team Jungle**, **Team Xecuter**, **Octal450**, **J-Runner-With-Extras contributors**, **Mitchell Waite / mitchellwaite**, **Pheeeeenom / Mena**, **Balázs Triszka / balika011**, **X360Tools contributors** and everyone who documented Xbox 360 NAND, eMMC, RGH/JTAG and board-level repair.

MODI integration / project direction: **Kacper Lewandowski · modyfikatorcasper · Modyfikator89 · Modi · MODI Diagnostic Lab**.

Full acknowledgements: [CREDITS.md](CREDITS.md)

## Firmware source and licensing

The distributed MODI UF2 includes firmware derived from PicoFlasher work. Matching corresponding firmware source and required third-party notices remain available with the release for license compliance.

[Download firmware source / compliance archive](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip)

See also: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)

## Independent project

**Independent fan-made community project.** MODI Pico 2 Flasher X360 TURBO and MODI Diagnostic Lab are not affiliated with, sponsored by, endorsed by or approved by Microsoft or Xbox. Xbox and related trademarks belong to their respective owners and are used only to identify compatible hardware and document technical/service procedures.

[Full disclaimer](DISCLAIMER.md) · [Release status and hashes](docs/RELEASE_STATUS.md)

**Project page:** https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/

