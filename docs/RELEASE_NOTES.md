# MODI Pico 2 Flasher X360 TURBO — 0.9.0 Beta (draft)

Preserved firmware TURBO baseline 2026-10-04 and tested MODI Setup packaging.
No binary was recompiled for this release preparation. SHA256SUMS.txt identifies
the exact installer, UF2 and corresponding firmware source archive.

Includes MODI recognition/panel, separate operation timers, memory labels,
connection cleanup, and project branding. Historical hardware measurements:
16 MB NAND ~19 s READ / ~24 s WRITE; Jasper BB tested 64 MiB + spare
76.890–76.955 s READ / 90.171 s WRITE; Corona eMMC tested 48 MiB
56.198–57.792 s READ / 48.310 s WRITE. Results vary with hardware and wiring;
they are not new tests of the installer-generated executable.

## Matching firmware source

The UF2 is accompanied in this same release by
`MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.0.zip`, with preserved GPL texts,
firmware C/header/PIO/CMake inputs, original SDK/TinyUSB source archives and
BUILD.md. Publish this archive alongside UF2 whenever publishing the draft.
SHA256 of the source archive:
`042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8`.

Setup requires the user's compatible J-Runner 3.4.0.7 installation and first-run
Internet access. It creates JRunner.MODI.exe locally; original JRunner.exe is
preserved. It embeds an extractable MIT/MODI source patch needed for local
building. A full J-Runner package, separate J-Runner source tree, firmware
tool binaries and unclear third-party DLLs are not included.

## Pending final QA

Exact public Setup → local JRunner.MODI → detection → READ → known-good WRITE
→ physical READ BACK and compare → console boot → another operation without
restarting J-Runner. Genuine application screenshot also remains pending.
No new hardware test was performed in release preparation. This remains a
draft Beta, not a Stable or final 1.0 claim.

Audio/Sonus: COMING SOON. DirtyJTAG and UART: PLANNED. HANA: RESEARCH.
Upstream support: PROPOSED. Credits and original licenses remain included.

## PL

To szkic wydania 0.9.0 Beta. Zachowuje sprawdzoną bazę TURBO i instalator bez
rekompilacji. Archiwum odpowiadających źródeł GPL należy opublikować razem
z UF2. Końcowy test dokładnej wersji z instalatora i prawdziwy screenshot
czekają; starsze pomiary nie są nowym testem tego wydania. Licencje i credits
pozostają dołączone. Funkcje FLASHSHIP zachowują statusy planowane.

License status / Licencje: inherited headers specify GPLv2; inherited LICENSE contains GPLv3. Both are preserved, without relicensing. Upstream provenance review remains open before final firmware publication. See the source archive LICENSE-VERSION-NOTICE.md.
