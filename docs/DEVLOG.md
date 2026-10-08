# DEVLOG / LAB NOTES

[Polski](DEVLOG_PL.md) · [Project agreements](PROJECT-AGREEMENTS.md) · [Website journal](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/#devlog)

Statuses: **IDEA / RESEARCH / PROTOTYPE / TESTED / VERIFIED**. VERIFIED requires scope and evidence.

## 2026-10-08 — from a simple flasher to FLASHSHIP + X360 ULTIMATE

**Module:** architecture / project history  
**Status:** RESEARCH — target system; TESTED — listed TURBO transfers; PROTOTYPE — additional Alpha profiles  
**Versions:** TURBO v0.9.1-stable, additional profiles v1.0.0-alpha.1  
**Configuration:** RP2350 / Pico 2 and J-Runner integration. Results apply to individual tested boards and ranges.

### Starting point

A simple, inexpensive flasher built on community PicoFlasher and J-Runner work. The first goal was concrete: NAND/eMMC read and write, visible progress, separate READ/WRITE timers and data comparison. Proven community components provided the foundation; MODI develops integration and usability.

### TURBO and unsuccessful experiments

Firmware and host optimizations included PIO/DMA transfers, pipelining and checked page/sector acknowledgments. Faster variants were not always stable. Tests included interrupted eMMC reads, incorrect Flash Config, stopped writes and a NAND comparison exception. One eMMC issue was traced to a damaged console. Interrupted transfers are not valid benchmarks.

Lesson: elapsed time alone is insufficient. A complete transfer, matching dumps, write readback and console boot are required within the specific test. Preserve the working base separately from experiments.

### Results recorded in the public table

| Memory / range | READ | WRITE | Scope |
|---|---:|---:|---|
| 16 MB NAND | ~19 s | ~24 s | Approximate tested transfer times. |
| Jasper Big Block, 64 MiB + spare | 76.890–76.955 s | 90.171 s | Two reads matched byte for byte; Write Successful alone does not replace readback. |
| Corona eMMC, 48 MiB | 56.198–57.792 s | 48.310 s | TURBO table results, not a full RGH benchmark. |

New assumptions do not overwrite recorded results. No new hardware tests were performed for this entry.

### Names

**FLASHSHIP** is the physical RP2350 device — FLASH + FLAGSHIP. **X360 ULTIMATE** is the complete target system. **TURBO** is its fast NAND/eMMC module.

**ONE DEVICE. ONE HEADER. ONE SOFTWARE.**

Current Alpha runs separate UF2 profiles. Additional GPIO supports development of Audio/Sonus, MODI Chip Flasher, UART/COM and HANA/SMBus LIVE. Unified firmware and software are not yet a verified complete product.

### Next stages

Automatic RGH: two dumps → compare → XeLL → flash → boot → CPU Key → build image → flash → verify. Approximately 18 + 18 + 24 = 60 seconds describes only the estimated memory path to XeLL. Complete automation and service time remain goals.

Conversions cover separate Corona V2/V4 4 GB paths, Winchester with required console data, and Jasper BB 256/512 MB — images for physical replacement with 16 MB NAND. DVD Remarry remains RESEARCH.

### Documentation

Our own FLASHSHIP front/back photographs and point macros will replace temporary reference photographs. Preserve sources and attribution until replacement. Label the device MODI FLASHSHIP on final diagrams.

### Our own contribution

An original project should make a meaningful contribution: new capabilities, wider access or improvements that were previously missing. Research and reverse engineering take time, often weeks or years before a small advance opens the next path. MODI develops a coherent service tool and its own solutions while acknowledging the work of others.

### Next step / VERIFIED gate

Shared modes require hardware validation: Audio backup/write/readback/play, chip IDCODE/program/verify, UART and concurrent SMBus. Automatic RGH and each conversion need a complete scenario, readback and boot confirmation. Record version, configuration and an evidence link without dumps, keys or customer data.

## Template for the next entry

- Date / module / status:
- Firmware and host version:
- Hardware configuration and range:
- Hypothesis:
- Trial / observation:
- Result and evidence:
- Failure / solution:
- Next step:

## Levy's principle

Do not reinvent the wheel.
