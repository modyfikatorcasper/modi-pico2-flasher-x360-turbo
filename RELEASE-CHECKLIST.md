# Release Checklist — MODI Pico 2 Flasher X360 TURBO

Use this checklist before publishing a public release.

## Files

- [ ] `MODI-Setup.exe` is the final tested build.
- [x] `MODI-Pico2-Flasher-X360-TURBO.uf2` matches the documented firmware version.
- [x] `SHA256SUMS.txt` contains hashes of every public binary.
- [ ] Matching GPL-compliant firmware source is available and linked.
- [x] No full J-Runner package is included.
- [x] No development workspace/source tree is included, except firmware source where legally required.
- [x] No private dumps, CPU keys, customer files, build cache, SDK or NuGet cache are included.
- [x] No third-party DLL with unclear redistribution rights is included.

## Documentation

- [x] English README is current.
- [x] Polish README is current.
- [ ] Polish installation manual is complete.
- [ ] English installation manual is complete.
- [x] FLASHSHIP roadmap is current.
- [x] Audio / Sonus is still marked `COMING SOON` unless real hardware testing is complete.
- [x] Credits are visible.
- [x] Disclaimer is visible.
- [ ] Original third-party license texts remain unchanged.
- [ ] Any Polish license translation is clearly marked informational/non-binding.

## Visuals

- [ ] Real `JRunner.MODI.exe` screenshot is present.
- [x] No test render is presented as a real running-session screenshot.
- [x] MODI logo is present.
- [x] HIGH SPEED → TURBO transition GIF is present.
- [ ] Visual style matches MODI MAPS language but uses neon green / black / dark grey.

## Final hardware smoke test

Using the exact public `MODI-Setup.exe`:

- [ ] select compatible J-Runner 3.4.0.7
- [ ] build/install `JRunner.MODI.exe`
- [ ] original `JRunner.exe` remains unchanged
- [ ] MODI Flasher is detected
- [ ] READ succeeds
- [ ] dump is correct / expected comparison succeeds
- [ ] WRITE known-good image succeeds
- [ ] READ BACK / binary compare succeeds
- [ ] console boots
- [ ] another operation can start without restarting J-Runner

## Claims

- [x] Hardware benchmarks are clearly labelled as tested-hardware results.
- [x] No installer benchmark claim is implied.
- [x] No “world's fastest” claim unless backed by a public current comparison.
- [ ] Current safe wording is used: “one of the fastest low-cost Xbox 360 flashing solutions we have tested.”
- [ ] ~$5–6 wording clearly refers to the core development board only.

## Release integrity

- [ ] GitHub Release hash matches `SHA256SUMS.txt` exactly.
- [x] Release notes list firmware and MODI Setup versions.
- [ ] Release notes link the exact corresponding firmware source.
- [ ] Changelog is updated.

## Staging result — 2026-10-04

Draft Beta release created: [MODI Pico 2 Flasher X360 TURBO — 0.9.0 Beta](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/untagged-e616676bca8f529a3867).
GitHub Actions staging succeeded. GitHub-reported SHA256 digests for Setup,
UF2 and the matching source archive equal the local hashes. Media and document
Git blob hashes were verified against main. Binaries are draft assets; main
contains documentation/media/required notices and release automation only.

Still open: genuine screenshot (capture tool timeout), final hardware smoke test
of the exact installer-generated executable, and upstream GPLv2-header/GPLv3-
LICENSE provenance review. Original notices are retained without relicensing.
The Setup embedded MIT/MODI source patch remains necessary for local building;
separate J-Runner sources are not published.

PL: Szkic Beta jest utworzony; hashe plików na GitHubie są zgodne. Czekają
prawdziwy screenshot, końcowy test sprzętowy dokładnej wersji z instalatora
oraz wyjaśnienie rozbieżności GPLv2/GPLv3 upstream. Główne repo nie zawiera
osobnych źródeł J-Runnera ani workspace'u.

