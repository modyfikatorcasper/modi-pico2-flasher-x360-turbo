# AGENT HANDOFF — MODI Pico 2 Flasher X360 TURBO

This repository is the **public release/product repository** for MODI Pico 2 Flasher X360 TURBO.

The agent should publish only end-user release material here.

## Target repository

`modyfikatorcasper/modi-pico2-flasher-x360-turbo`

## Upload only what users need

Public release contents should be limited to:

- `MODI-Setup.exe`
- `MODI-Pico2-Flasher-X360-TURBO.uf2`
- `SHA256SUMS.txt`
- user documentation
- release notes / changelog
- visual assets: logo, High Speed → TURBO GIF, real application screenshot, wiring graphics
- original third-party license texts / notices required by redistributed components
- a clear link or matching archive containing the GPL-compliant corresponding source for the distributed firmware UF2

## DO NOT upload

- full J-Runner source tree
- full modified J-Runner package
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

## J-Runner distribution model

The public repository should distribute **MODI Setup**, not a repackaged full third-party J-Runner bundle.

MODI Setup should continue to:

1. ask the user for their compatible J-Runner installation;
2. validate it;
3. obtain pinned build dependencies;
4. build the MODI integration locally;
5. produce `JRunner.MODI.exe` next to the original;
6. leave `JRunner.exe` unchanged.

## Firmware source rule

The main public repo should stay clean, but the modified firmware UF2 is derived from GPL-licensed PicoFlasher work. Therefore the exact corresponding firmware source for every distributed UF2 must remain available in a GPL-compliant form.

Preferred options:

- separate dedicated firmware-source repository, or
- matching source archive attached to the same release.

The README and each release must link to the corresponding source.

## Required release QA before v1.0

Perform at least one smoke test using the exact public `MODI-Setup.exe`:

`Setup → JRunner.MODI.exe → device detect → READ → WRITE known-good image → READ BACK / compare → console boot → next operation without restarting J-Runner`

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
