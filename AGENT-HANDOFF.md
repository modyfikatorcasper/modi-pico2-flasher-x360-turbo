# AGENT HANDOFF — MODI Pico 2 Flasher X360 TURBO

This repository is the **public release/product repository** for MODI Pico 2 Flasher X360 TURBO.

The agent should publish only end-user release material here.

## Target repository

`modyfikatorcasper/modi-pico2-flasher-x360-turbo`

## FINAL USER EXPERIENCE — NON-NEGOTIABLE

The public release must be a **ready-to-use package**.

The user must **NOT** need to compile J-Runner locally, install a .NET SDK, download NuGet packages, run MSBuild, use Python, or understand the build process.

Target user flow:

1. download the release package;
2. flash the included MODI UF2 to Pico 2 / RP2350;
3. run `MODI-Setup.exe`;
4. installer automatically prepares `JRunner.MODI.exe`;
5. launch it and use the flasher.

No developer environment. No local source build. No manual dependency setup.

### Preferred technical model

To avoid redistributing third-party files whose redistribution status is unclear, `MODI-Setup.exe` should work as a **one-click binary patcher/installer**, not as a local source compiler.

Preferred behaviour:

- automatically detect a compatible J-Runner with Extras 3.4.0.7 installation; OR
- automatically download the exact pinned official upstream J-Runner release from its official source when legally/technically appropriate;
- verify version and SHA256;
- copy the original so it remains untouched;
- apply only the MODI-owned binary patch/resources needed for the integration;
- create a ready `JRunner.MODI.exe`;
- create a shortcut if appropriate;
- finish with a clear `Ready / Gotowe` state.

Fallback may allow the user to select `JRunner.exe` manually, but the user must never compile anything.

The final 0.9.1 Beta installer is an offline compiled patcher. It requires no SDK, compiler, NuGet, Python or local source build; preserve the tested Setup and UF2 bytes during packaging cleanup.

## Ready release package

In addition to individual advanced downloads, prepare one obvious package:

`MODI-Pico2-Flasher-X360-TURBO-vX.Y.Z.zip`

It should contain only end-user files such as:

- `MODI-Setup.exe`
- `MODI-Pico2-Flasher-X360-TURBO.uf2`
- `START-HERE-PL.txt`
- `START-HERE-EN.txt`
- `SHA256SUMS.txt`
- required notices/licenses

The user should be able to download one ZIP, extract it and start.

## Public release asset policy — exactly four files

1. `MODI-Pico2-Flasher-X360-TURBO.uf2` — primary download.
2. `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip` — complete installation package.
3. `MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip` — firmware source/license compliance only.
4. `SHA256SUMS.txt`.

Setup is inside the installation ZIP, never a separate release asset. Required licenses/notices are inside installation and SOURCE ZIPs, never individual assets. Documentation and visual assets belong to the repository/page. No release-directory wildcard uploads.

SOURCE contains complete modified firmware, required SDK/TinyUSB source material, original notices, build inputs/instructions and SHA256-SOURCE.txt. No Setup, JRunner.MODI or private application/integration source.

README/landing page buttons: DOWNLOAD UF2 → DOWNLOAD COMPLETE PACKAGE → MANUAL. A small bottom text link provides Firmware source / license compliance.

## Project agreements — current authority

Follow [PROJECT-AGREEMENTS.md](docs/PROJECT-AGREEMENTS.md) / [Polski](docs/PROJECT-AGREEMENTS_PL.md), established 2026-10-08. FLASHSHIP is the RP2350 hardware (FLASH + FLAGSHIP); X360 ULTIMATE is the complete target system; TURBO is the NAND/eMMC module. Preserve tested binary bytes.

Keep DEVLOG / LAB NOTES on GitHub Pages current with IDEA / RESEARCH / PROTOTYPE / TESTED / VERIFIED, scoped results, failures and next steps. Never promote a development target to a tested capability without evidence.

## Media policy

Use current ULTIMATE branding. The High Speed → TURBO transition GIF/MP4 is retired. Label the board MODI FLASHSHIP. Replace temporary third-party photos with our own front/back RP2350-Plus and point macros before final documentation; retain attribution until replacement.

## DO NOT upload

- full J-Runner source tree
- application development source code
- full modified J-Runner package unless redistribution has been explicitly cleared
- development workspace
- internal source dumps
- build cache
- .NET SDK
- NuGet cache
- private logs
- CPU keys
- NAND/eMMC dumps
- customer data
- temporary scripts
- debug binaries
- third-party DLLs whose redistribution rights are not confirmed
- test render presented as a real application screenshot

The only source that must remain available publicly is source required by applicable licenses, especially the corresponding source for the distributed GPL-derived firmware.

## Firmware source rule

The main public repo should stay clean, but the modified firmware UF2 is derived from GPL-licensed PicoFlasher work. Therefore the exact corresponding firmware source for every distributed UF2 must remain available in a GPL-compliant form.

Preferred options:

- separate dedicated firmware-source repository, or
- matching source archive attached to the same release.

The README and each release must link to the corresponding source.

## Required release QA before v1.0

Perform at least one smoke test using the exact final public `MODI-Setup.exe` and exact release package:

`fresh PC/folder → Setup → ready JRunner.MODI.exe → device detect → READ → WRITE known-good image → READ BACK / compare → console boot → next operation without restarting J-Runner`

Also verify:

- no SDK is downloaded or required;
- no compiler is required;
- no source tree is created for the user;
- original `JRunner.exe` remains unchanged;
- final ZIP contains everything a normal user needs;
- hashes match uploaded release assets.

Do not treat previous hardware benchmarks as a new installer benchmark.

## Visual style

Follow the same design language as MODI MAPS:

- dark background
- technical/service-tool presentation
- strong cards and clean sections
- PL / EN
- mobile-friendly

But this project uses **neon green + black + dark grey** as its visual identity.

Use current MODI X360 ULTIMATE branding, with FLASHSHIP as hardware and TURBO as the flashing module.

## Public positioning

Repair-first / Right to Repair.

Do not claim official Microsoft/Xbox affiliation.
Do not claim upstream J-Runner endorsement.
Do not claim “world's fastest” until a public comparative benchmark supports it.

Current safe wording:

> One of the fastest low-cost Xbox 360 flashing solutions we have tested.

## Credits must remain prominent

Always acknowledge:

- Team Jungle
- Team Xecuter
- Octal450
- J-Runner-With-Extras organization and contributors
- Mitchell Waite / mitchellwaite
- Pheeeeenom / Mena for current release/distribution ecosystem contribution
- Balázs Triszka / balika011
- X360Tools contributors
- MODI Diagnostic Lab / Modyfikator89 for MODI integration/project

Do not imply that any upstream contributor endorses MODI.

## Roadmap and status

Use **MODI X360 ULTIMATE — What's Next / Co dalej** for the target system. MODI FLASHSHIP identifies the physical hardware.

Current Alpha additional functions remain prototypes with hardware validation pending. Public feature name: **MODI Chip Flasher**; acknowledge DirtyJTAG technology in credits/licenses. Automatic RGH, memory conversions and unified modes remain development goals. DVD Remarry remains research. Consult [ULTIMATE](docs/ULTIMATE.md) for current scope and [DEVLOG](docs/DEVLOG.md) for evidence. Do not announce Audio/chip programming or full automation as complete without hardware tests.
