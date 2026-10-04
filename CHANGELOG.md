# Changelog

## v0.9.1 Beta — 2026-10-04

- Offline one-click compiled-IL patcher; no end-user build tooling.
- One ready ZIP with Setup, unchanged TURBO UF2, START-HERE PL/EN, hashes and notices.
- Official upstream J-Runner 3.4.0 r7 link and exact original SHA256 pin.
- Preserved original J-Runner and embedded third-party resources.
- Verified clean-folder install, 753 donor method matches and 18 offline integration tests.
- Actual final application launch and MODI Turbo device recognition.
- Matching GPL firmware source supplied separately with unchanged source bytes.
- Static logo and one GIF retained; duplicate MP4 removed from the repository.
- Full physical final-package smoke test and genuine screenshot remain pending before v1.0.


## v0.9.0 Beta — planned public release

- MODI Pico 2 Flasher X360 TURBO branding.
- MODI device identity detection in J-Runner integration.
- Separate MODI information panel.
- Separate READ / WRITE / VERIFY timing.
- NAND/eMMC operation label fixes.
- connection cleanup and re-detection improvements.
- local MODI Setup distribution model instead of repackaging the full third-party J-Runner bundle.
- bilingual EN / PL documentation.
- MODI FLASHSHIP roadmap.

### Hardware benchmark context

Previously measured on tested hardware:

- 16 MB NAND: ~19 s READ / ~24 s WRITE
- Jasper Big Block tested 64 MiB + spare range: 76.890–76.955 s READ / 90.171 s WRITE
- Corona eMMC tested 48 MiB range: 56.198–57.792 s READ / 48.310 s WRITE

These are historical tested-hardware results, not installer benchmarks.

### Before v1.0

A final hardware smoke test must be performed using the exact public MODI Setup build and resulting `JRunner.MODI.exe`.

