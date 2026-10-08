# FLASHSHIP / ULTIMATE — project agreements

Established by the project owner on **8 October 2026**. “Back to FLASHSHIP / ULTIMATE” refers to these agreements.

[Polski](PROJECT-AGREEMENTS_PL.md) · [DEVLOG / LAB NOTES](DEVLOG.md) · [Current ULTIMATE state](ULTIMATE.md)

## Names and philosophy

| Name | Meaning |
|---|---|
| **MODI FLASHSHIP** | Physical RP2350 board/device. FLASH + FLAGSHIP. |
| **MODI X360 ULTIMATE** | The complete target service system and software. |
| **TURBO** | Fast NAND/eMMC module, not the name of the whole ecosystem. |
| **MODI Chip Flasher** | Glitch-chip programming feature; DirtyJTAG is acknowledged in credits and licenses. |

**ONE DEVICE. ONE HEADER. ONE SOFTWARE.**

An original project should make a meaningful contribution: new capabilities, wider access or improvements that were previously missing. Research and reverse engineering take time, often weeks or years before a small advance opens the next path. MODI develops a coherent service tool and its own solutions while acknowledging the work of others.

This is the target architecture. Current Alpha uses separate UF2 profiles; unified firmware and automatic mode switching still require implementation and validation.

## Automatic RGH — target

Two dumps → compare → create XeLL → flash → boot console → capture CPU Key automatically → validate key → build image automatically → flash final NAND → readback / verify.

Two matching backups, correct memory identification and console-data validation are gates before writing. Uncertain input stops the operation.

At approximately 18 s + 18 s + 24 s, the memory path to XeLL takes approximately **60 s**. This is an estimate from transfer times, not a measured complete Automatic RGH run. The public TURBO table continues to report approximately 19 s READ and 24 s WRITE for tested 16 MB NAND.

The service goal is several to a dozen or so minutes for an experienced technician, including disassembly and soldering, with an almost unattended software workflow. This is not a current guarantee or measured result.

## Modules

TURBO NAND/eMMC, Audio/Sonus, MODI Chip Flasher, UART/COM, HANA/SMBus LIVE, then memory conversions and further functions.

Automatic CPU Key capture requires a supported XeLL data path; LAN is the current alternative. SMBus/HANA traffic alone provides neither CPU Key nor a complete HDMI test.

## Conversions — images for physical memory replacement

- Corona 4 GB → 16 MB NAND: separate V2 and V4 paths.
- Winchester → 16 MB NAND: appropriate console data acquired through a supported method such as Bad Update; not classic RGH.
- Jasper Big Block 256 MB → 16 MB NAND.
- Jasper Big Block 512 MB → 16 MB NAND.

Maximize automation while checking input data, readback and console boot for each combination. Conversions are in development. DVD Remarry remains a later research project.

## Chip programming and power

Aim to avoid an additional programmer. A loose chip may use FLASHSHIP 3.3 V after confirming its voltage and load match the board. Do not connect a second power supply to a chip already powered by the console. Follow the wiring map for the specific chip model.

## Documentation and our own photographs

Label the device **MODI FLASHSHIP** on diagrams; add RP2350-Plus where the hardware model matters.

Take our own front/back RP2350-Plus photographs, then macro photographs of all console and chip points. Third-party photographs are temporary references; final documentation should use our own photographs. Preserve attribution until replacement. Never describe a third-party photograph as ours.

## DEVLOG / LAB NOTES

GitHub Pages records ideas, development, tests, failures and solutions.

| Status | Meaning |
|---|---|
| IDEA | Idea without confirmed implementation. |
| RESEARCH | Documentation and feasibility investigation. |
| PROTOTYPE | Existing prototype with incomplete validation. |
| TESTED | Test performed within a stated scope and configuration. |
| VERIFIED | Result confirmed with a recorded method and evidence, such as compare/readback. |

Each entry records date, module, status, version, configuration, observation, result and next step. VERIFIED applies to a specific test, not automatically the whole product.

First major entry: from a few-dollar flasher to **FLASHSHIP + X360 ULTIMATE**.

## Publishing

Users receive ready files and a simple installation. Private MODI application code stays private. Required corresponding firmware sources and notices remain available under applicable licenses. These agreements do not change tested UF2/Setup bytes or test results.

## Levy's principle

Do not reinvent the wheel.
