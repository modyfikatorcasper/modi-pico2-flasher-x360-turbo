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

The current Beta installer that downloads an SDK and performs a local source build is **transitional and is NOT acceptable as the final public release UX**.

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

## Upload only what users need

Public release contents should be limited to:

- ready `MODI-Setup.exe`
- ready `MODI-Pico2-Flasher-X360-TURBO.uf2`
- one ready end-user ZIP package
- `SHA256SUMS.txt`
- user documentation
- release notes / changelog
- visual assets: logo, **one High Speed → TURBO GIF**, real application screenshot, wiring graphics
- original third-party license texts / notices required by redistributed components
- a clear link or matching archive containing the GPL-compliant corresponding source for the distributed firmware UF2

## Media policy

Keep the public GitHub clean.

Use:

- one static MODI TURBO logo;
- one `HIGH SPEED → TURBO` GIF.

Do **not** keep the duplicate 1080p MP4 transition video in the repository/page. The MP4 is for social/video editing, not necessary for the GitHub product page.

The GIF should be optimized for web/GitHub size if possible while keeping the branding readable.

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

Use the existing MODI Pico 2 Flasher X360 HIGH SPEED → TURBO branding.

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

## Roadmap label

Use:

**MODI FLASHSHIP — What's Next / Co dalej**

Current statuses:

- Audio / Sonus — COMING SOON
- DirtyJTAG / glitch-chip programmer — PLANNED
- UART / COM monitor — PLANNED
- HANA diagnostics — RESEARCH
- native upstream J-Runner support — PROPOSED

Do not implement or announce Audio as complete until hardware tests are finished.
