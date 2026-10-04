# MODI Pico 2 Flasher X360 TURBO — 0.9.1 Beta

## Download

### 1. Flash your Pico 2
[Download MODI Pico 2 TURBO UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2)

### 2. Install MODI J-Runner integration
[Download complete installation package](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip)

The installation ZIP contains MODI-Setup.exe, the unchanged UF2, START-HERE PL/EN, internal SHA256 checks and required binary notices/licenses. Setup works offline with a complete, verified J-Runner with Extras 3.4.0.7 installation and creates JRunner.MODI.exe while preserving the original. No compiler, SDK, NuGet, Python or application source build is needed.

PL: Wgraj UF2 na Pico 2 w BOOTSEL, następnie rozpakuj pełną paczkę i uruchom MODI-Setup.exe. Instalator wykorzystuje Twoją pełną, zgodną instalację J-Runnera. Binaria Setup i UF2 oraz kod NAND/eMMC i czasy pozostają bez zmian.

[Manual EN](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/blob/main/docs/INSTALL.md) · [Instrukcja PL](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/blob/main/docs/INSTALL_PL.md) · [Official J-Runner 3.4.0 r7 base](https://github.com/J-Runner-With-Extras/J-Runner-with-Extras/releases/tag/V3.4.0-r7)

Setup version: **0.9.1-beta**. Firmware: **preserved MODI TURBO baseline 2026-10-04**, unchanged from the validated baseline. No new speed tuning is introduced by this packaging release.

## Verified in this release

- Exact ZIP extraction and all included hashes.
- Fresh-folder installation, original preservation, repeat installation and rejection of incompatible or incomplete upstream copies.
- 753 patched methods match the preserved integration; 18 offline integration tests pass.
- Actual final JRunner.MODI launch and attached Pico identification as MODI Turbo.
- Original embedded third-party library resources remain byte-for-byte unchanged.
- No full J-Runner, application source tree, private dumps, CPU keys or unclear third-party DLLs in the public package.

## Test status

This is a **public Beta**, not a Stable/v1.0 release. On 2026-10-04 the user confirmed: “TEST SA WYKONA WSZYSTKO DZIALA” (tests completed; everything works), in response to the final hardware smoke-test request. This is user-reported hardware confirmation; no new per-operation times or readback hashes were supplied. Previous hardware timings remain historical baseline results. A genuine application screenshot is pending; no simulated screenshot is substituted.

PL: Użytkownik potwierdził 2026-10-04 wykonanie testów i poprawne działanie. Potwierdzenie sprzętowe pochodzi od użytkownika; agent nie dopisuje nowych czasów ani hashy odczytu kontrolnego.

NAND 16 MB baseline: ~19 s READ / ~24 s WRITE.
Jasper Big Block, tested 64 MiB + spare range: 76.890–76.955 s READ / 90.171 s WRITE.
Corona eMMC, tested 48 MiB: 56.198–57.792 s READ / 48.310 s WRITE.
Results vary with hardware and wiring.

## Advanced / source compliance

[Download corresponding firmware source](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip)

One SOURCE ZIP contains complete modified firmware, matching SDK/TinyUSB source archives, build inputs and instructions, original license texts and notices. It contains no MODI Setup, JRunner.MODI or private application/integration source.

[SHA256SUMS.txt](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/SHA256SUMS.txt)

## Integrity

| Asset | SHA256 |
|---|---|
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip` | `E18BF9E6EAD0353842920D88362749FD1B4F5FFE8976DD11ADE7A37151240D53` |
| `MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip` | `9E26CB674949012C1C9B9E65BB68E91EE3FB98F4955EC90549143C9513A407D4` |
| `SHA256SUMS.txt` | `26089A402C0BF5877EBD56052ECE53E440B942939F7E8E99F162A6B0971DA181` |

## Licenses and credits

Matching firmware source and original license notices are provided alongside the UF2. Inherited PicoFlasher source headers specify GPLv2 while its inherited LICENSE is GPLv3; both original texts are preserved and provenance review remains open. No relicensing is claimed. This release does not redistribute the user's full J-Runner installation or unclear third-party components.

Credits: Team Jungle, Team Xecuter, Octal450, J-Runner-With-Extras contributors, Mitchell Waite, Pheeeeenom/Mena, Balázs Triszka, X360Tools contributors, 15432, MayaTelLabs, Raspberry Pi, TinyUSB, Jb Evain/Novell and MODI Diagnostic Lab / Modyfikator89. No endorsement or Microsoft/Xbox affiliation is implied.

Audio/Sonus: COMING SOON. DirtyJTAG/UART: PLANNED. HANA: RESEARCH. Upstream: PROPOSED.

