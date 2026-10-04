# MODI Pico 2 Flasher X360 TURBO — 0.9.1 Beta

## Pobierz / Download

**[Jedna gotowa paczka ZIP / Complete end-user package](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip)**

W ZIP-ie: instalator offline, UF2, START-HERE PL/EN, SHA256 i wymagane licencje.
The ZIP includes the offline installer, UF2, START-HERE PL/EN, SHA256 and required notices.

Setup wykrywa zgodnego J-Runnera with Extras 3.4.0.7 lub pozwala wskazać jego oryginalny JRunner.exe. Tworzy gotowy JRunner.MODI.exe, zachowując oryginał oraz istniejące pliki pomocnicze. Użytkownik nie potrzebuje kompilatora, SDK, NuGet, Python ani Internetu do instalacji MODI. Wymagana jest pełna oficjalna instalacja J-Runnera z folderami common i xeBuild.

Setup detects a compatible J-Runner with Extras 3.4.0.7 installation or accepts its original executable once. It creates ready JRunner.MODI.exe and preserves the original and support files. Installation is offline and requires no compiler, SDK, NuGet or Python. The complete official upstream installation with common and xeBuild folders is required.

[Oficjalny J-Runner 3.4.0 r7 / Official upstream base](https://github.com/J-Runner-With-Extras/J-Runner-with-Extras/releases/tag/V3.4.0-r7)

## Oddzielne pliki / Advanced downloads

- [MODI-Setup.exe](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Setup.exe)
- [Pico 2 TURBO UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2)
- [SHA256SUMS.txt](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/SHA256SUMS.txt)
- [Odpowiadające źródła firmware / Matching firmware source](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.1.zip)

Setup version: **0.9.1-beta**. Firmware: **preserved MODI TURBO baseline 2026-10-04**, unchanged from the validated baseline. No new speed tuning is introduced by this packaging release.

## Verified in this release

- Exact ZIP extraction and all included hashes.
- Fresh-folder installation, original preservation, repeat installation and rejection of incompatible or incomplete upstream copies.
- 753 patched methods match the preserved integration; 18 offline integration tests pass.
- Actual final JRunner.MODI launch and attached Pico identification as MODI Turbo.
- Original embedded third-party library resources remain byte-for-byte unchanged.
- No full J-Runner, application source tree, private dumps, CPU keys or unclear third-party DLLs in the public package.

## Test status

This is a **public Beta**, not a Stable/v1.0 release. Full READ → WRITE known-good image → physical READ BACK/compare → console boot → repeat operation on this exact installer-generated version remains pending. Previous hardware timings are historical baseline results, not new tests of this package. A genuine application screenshot is also pending; no simulated screenshot is substituted.

NAND 16 MB baseline: ~19 s READ / ~24 s WRITE.
Jasper Big Block, tested 64 MiB + spare range: 76.890–76.955 s READ / 90.171 s WRITE.
Corona eMMC, tested 48 MiB: 56.198–57.792 s READ / 48.310 s WRITE.
Results vary with hardware and wiring.

## Integrity

| File | SHA256 |
|---|---|
| `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip` | `D37B4C6449D128150F5E4F697130A18D66D28C7A4AC0FC0B0A4A443DB452BA4C` |
| `MODI-Setup.exe` | `40EC3430563DA2FC5B261A8D2BC3F62E6684D9CCB02453A2FFCCA03420CA2C2D` |
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.1.zip` | `042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8` |

## Licenses and credits

Matching firmware source and original license notices are provided alongside the UF2. Inherited PicoFlasher source headers specify GPLv2 while its inherited LICENSE is GPLv3; both original texts are preserved and provenance review remains open. No relicensing is claimed. This release does not redistribute the user's full J-Runner installation or unclear third-party components.

Credits: Team Jungle, Team Xecuter, Octal450, J-Runner-With-Extras contributors, Mitchell Waite, Pheeeeenom/Mena, Balázs Triszka, X360Tools contributors, 15432, MayaTelLabs, Raspberry Pi, TinyUSB, Jb Evain/Novell and MODI Diagnostic Lab / Modyfikator89. No endorsement or Microsoft/Xbox affiliation is implied.

Audio/Sonus: COMING SOON. DirtyJTAG/UART: PLANNED. HANA: RESEARCH. Upstream: PROPOSED.

