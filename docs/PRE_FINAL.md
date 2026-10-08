# MODI pre-final and final release milestone

[Polski](PRE_FINAL_PL.md) · [Audio and DirtyJTAG wiring](FLASHSHIP_WIRING.md)

The local pre-final package dated 8 October 2026 consolidates the tested TURBO baseline with existing Audio, DirtyJTAG and LIVE previews. [v0.9.1-beta](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta) remains the public release. Preview documentation and diagrams are public; full local JRunner.exe preview distribution still requires an audit.

## Package scope

| Component | Status |
|---|---|
| TURBO NAND/eMMC and MODI-Setup.exe | Tested binaries; original bytes and hashes preserved |
| Audio Sonus | Builds and offline tests passed; physical tests pending |
| DirtyJTAG ACE V3 / CoolRunner / Matrix | SVF/XSVF preview; chip tests pending |
| ACE V3+ / V4 / V5 Gowin | .fs backend not implemented |
| UART plus passive SMBus/HANA | Concurrent capture implemented in LIVE; hardware validation pending |
| XeLL over LAN | Local preview panel, key validation and local save |
| Image for physical replacement with NAND 16 MB | Final planned development feature; not implemented |

Setup still installs the existing baseline. The LIVE EXE is an additional preview for a separate copy of a complete installation. Audio/DirtyJTAG use the MODI-Flashship companion. One Pico runs one UF2 profile; no single firmware currently combines all programmers and capture functions.

## Final development feature

Confirmed scope: one click prepares an image for **physical replacement** of Corona eMMC or Jasper 256/512 MB NAND with a compatible 16 MB NAND. Each motherboard revision and target chip must have verified support before this function is offered.

Planned workflow:

1. Preserve original backups and require independently matching reads and hashes.
2. Identify revision, source geometry, ECC/spare, remaps and console identity; validate the CPU Key when required.
3. Establish compatibility of the physical 16 MB target, wiring, board configuration, bootloader and SMC.
4. Generate an image using this console's valid data and the target geometry, ECC and remapping.
5. Independently validate, write a new output file and produce a hash report. Unsupported combinations stop.

A compatible image must be rebuilt; truncation alone is insufficient. Software cannot change the physical memory interface or board configuration. Image preparation does not automatically flash the console. Target programming and full readback are separate operations after hardware verification.

## Final release requirements

Conversion needs image fixtures plus full write, matching readback and a real console boot for supported revisions. New modules require physical Audio, JTAG and simultaneous UART/SMBus tests. Host redistribution needs a completed audit or a patch/updater distribution.

The public release keeps four assets: primary UF2, complete installation ZIP, one SOURCE ZIP covering every distributed firmware profile, and SHA256SUMS.txt. Private MODI-Setup, J-Runner and MODI integration source remains outside the public repository.
