# Third-Party Notices / Informacje o komponentach zewnętrznych

This repository is an independent MODI release/integration project. It relies on or interoperates with third-party projects whose original authorship and licenses must remain visible.

## J-Runner / J-Runner with Extras

Upstream project: **J-Runner with Extras**.

Acknowledgements include:

- Team Jungle
- Team Xecuter
- Octal450
- J-Runner-With-Extras organization and contributors
- Mitchell Waite / mitchellwaite
- Pheeeeenom / Mena for current release/distribution ecosystem contribution

MODI integration is independent and must not be presented as an official upstream J-Runner with Extras feature unless that changes in the future.

The public MODI distribution should avoid redistributing a full third-party J-Runner package when license status of bundled dependencies is unclear. The preferred model is `MODI-Setup.exe`, which works from the user's compatible J-Runner installation and patches an audited copy offline.

## PicoFlasher

Original PicoFlasher work: **Balázs Triszka / balika011**.

Further development: **X360Tools contributors**.

The MODI firmware is derived from GPL-licensed PicoFlasher work. If a modified UF2 is distributed, its exact corresponding source must be made available in a GPL-compliant form.

The main public release repository may remain binary/documentation focused, but each firmware release must provide a clear link to the matching source repository or a matching source archive.

## Original license texts

Original third-party license texts must be preserved unchanged when required.

Any Polish translation is only an informational convenience translation and must be marked clearly:

> Nieoficjalne tłumaczenie informacyjne. W przypadku rozbieżności wiążący jest oryginalny tekst licencji.

> Unofficial convenience translation. In case of any discrepancy, the original license text governs.

## No endorsement implied

Listing a project, author or contributor here does not imply sponsorship, endorsement or affiliation with MODI Diagnostic Lab / Modyfikator89.


## Included notices / Dołączone informacje prawne

Original legal texts are copied byte-for-byte to `licenses/`:
- LICENSE-JRunner.txt — MIT notice for the limited modified J-Runner portions in Setup.
- LICENSE-MODI.txt — MODI integration/installer notice.
- LICENSE-Firmware-GPL-3.0.txt — original PicoFlasher GPLv3.
- LICENSE-Pico-SDK.txt — Raspberry Pi Pico SDK BSD terms.
- LICENSE-TinyUSB.txt — TinyUSB MIT notice.

The firmware source archive retains the additional notices inside the original
SDK/TinyUSB archives and existing source headers. GCC/newlib are general-purpose
toolchain/system-library inputs; compiler binaries are not redistributed here.
Source lineage also includes 15432 and MayaTelLabs/Pico2Flasher. Credits do not
imply endorsement. Setup embeds a compiled IL payload containing only audited MIT/MODI types and its own logo/build resources. Separate J-Runner source files are not published.

Additional runtime notices: licenses/LICENSE-Newlib.txt (newlib 4.4.0), LICENSE-GCC-RUNTIME-EXCEPTION.txt, and LICENSE-GPL-2.0.txt. PicoFlasher source headers specify GPLv2 although the inherited LICENSE is GPLv3. Original notices are retained; no upstream relicensing is claimed. Resolve provenance before final firmware publication.


## Mono.Cecil 0.11.6

The patcher embeds Mono.Cecil 0.11.6, copyright Jb Evain and Novell, under MIT. Original notice: `licenses/LICENSE-Cecil.txt`. Source: https://github.com/jbevain/cecil/tree/0.11.6 .

Existing third-party DLLs and restricted/unclear audio, registry and ZIP code are read from the user installation and preserved locally; they are absent from the public patch payload. No full J-Runner executable is redistributed.
