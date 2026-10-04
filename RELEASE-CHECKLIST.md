# Release Checklist — MODI Pico 2 Flasher X360 TURBO

Use this checklist before publishing a public release.

## Final package UX

- [ ] The public release is a **ready-to-use one-click package**.
- [ ] User does **not** need to install/download a .NET SDK.
- [ ] User does **not** need NuGet, MSBuild, Python or any compiler.
- [ ] User does **not** perform a local source build.
- [ ] `MODI-Setup.exe` automatically prepares a ready `JRunner.MODI.exe` from a verified compatible upstream J-Runner copy.
- [ ] Original `JRunner.exe` remains unchanged.
- [ ] A single end-user ZIP exists: `MODI-Pico2-Flasher-X360-TURBO-vX.Y.Z.zip`.
- [ ] ZIP contains Setup, UF2, START-HERE PL/EN, hashes and required notices.

## Files

- [ ] `MODI-Setup.exe` is the final tested one-click build.
- [x] `MODI-Pico2-Flasher-X360-TURBO.uf2` matches the documented firmware baseline.
- [x] `SHA256SUMS.txt` contains hashes of every public binary.
- [ ] Matching GPL-compliant firmware source is available and linked.
- [ ] Final one-click ZIP is uploaded and hashed.
- [x] No full J-Runner package is included unless redistribution is explicitly cleared.
- [x] No application development workspace/source tree is included.
- [x] No private dumps, CPU keys, customer files, build cache, SDK or NuGet cache are included.
- [x] No third-party DLL with unclear redistribution rights is included.

## Documentation

- [x] English README exists.
- [x] Polish README exists.
- [ ] README EN/PL is updated to describe the final **one-click installer**, not the transitional local-build Beta.
- [ ] Polish installation manual describes the final one-click flow.
- [ ] English installation manual describes the final one-click flow.
- [x] FLASHSHIP roadmap is current.
- [x] Audio / Sonus is marked `COMING SOON` unless real hardware testing is complete.
- [x] Credits are visible.
- [x] Disclaimer is visible.
- [ ] Original third-party license texts remain unchanged.
- [ ] Any Polish license translation is clearly marked informational/non-binding.

## Visuals

- [ ] Real `JRunner.MODI.exe` screenshot is present.
- [x] No test render is presented as a real running-session screenshot.
- [x] MODI logo is present.
- [x] HIGH SPEED → TURBO transition GIF is present.
- [ ] Duplicate transition MP4 is removed from the GitHub product page/repository; keep MP4 for external video/social editing only.
- [ ] GIF is reasonably optimized for web size.
- [ ] Visual style matches MODI MAPS language but uses neon green / black / dark grey.

## Final hardware smoke test

Using the exact final public ZIP and `MODI-Setup.exe`:

- [ ] start from a clean test folder / fresh-user scenario
- [ ] installer obtains/detects compatible J-Runner 3.4.0.7 automatically or with one simple file selection
- [ ] no compiler/SDK/source build occurs
- [ ] ready `JRunner.MODI.exe` is created/installed
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
- [x] Current safe wording is used: “one of the fastest low-cost Xbox 360 flashing solutions we have tested.”
- [x] ~$5–6 wording clearly refers to the core development board only.

## Release integrity

- [ ] GitHub Release hashes match `SHA256SUMS.txt` exactly.
- [ ] Release notes list final Setup and firmware versions.
- [ ] Release notes link the exact corresponding firmware source.
- [ ] Changelog is updated.
- [ ] Direct download buttons point to the final public release assets.

## Current staging state — 2026-10-04

A draft `v0.9.0-beta` release exists with staged Setup, UF2, hashes, licenses and corresponding firmware source.

Important: the currently staged Setup still uses the earlier local-build model. It is a **transitional Beta candidate**, not the desired final user experience.

Before public release, replace it with the one-click installer/patcher described in `AGENT-HANDOFF.md`, then update README/manuals and perform the exact final-package hardware smoke test.

PL: obecny szkic Beta zawiera przygotowane pliki, ale instalator nadal używa starego modelu lokalnego builda. Przed publicznym wydaniem ma zostać zastąpiony gotowym instalatorem typu one-click, bez SDK, kompilatora, NuGet i ręcznego składania czegokolwiek przez użytkownika.
