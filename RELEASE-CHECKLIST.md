# Release Checklist — MODI Pico 2 Flasher X360 TURBO

Use this checklist before publishing a public release.

## Final package UX

- [x] The public release is a **ready-to-use one-click package**.
- [x] User does **not** need to install/download a .NET SDK.
- [x] User does **not** need NuGet, MSBuild, Python or any compiler.
- [x] User does **not** perform a local source build.
- [x] `MODI-Setup.exe` automatically prepares a ready `JRunner.MODI.exe` from a verified compatible upstream J-Runner copy.
- [x] Original `JRunner.exe` remains unchanged.
- [x] A single end-user ZIP exists: `MODI-Pico2-Flasher-X360-TURBO-vX.Y.Z.zip`.
- [x] ZIP contains Setup, UF2, START-HERE PL/EN, hashes and required notices.

## Files

- [x] `MODI-Setup.exe` is the final tested one-click build.
- [x] `MODI-Pico2-Flasher-X360-TURBO.uf2` matches the documented firmware baseline.
- [x] `SHA256SUMS.txt` contains hashes of every public binary.
- [ ] Matching GPL-compliant firmware source is available and linked.
- [x] Final one-click ZIP is uploaded and hashed.
- [x] No full J-Runner package is included unless redistribution is explicitly cleared.
- [x] No application development workspace/source tree is included.
- [x] No private dumps, CPU keys, customer files, build cache, SDK or NuGet cache are included.
- [x] No third-party DLL with unclear redistribution rights is included.

## Documentation

- [x] English README exists.
- [x] Polish README exists.
- [x] README EN/PL is updated to describe the final **one-click installer**, not the transitional local-build Beta.
- [x] Polish installation manual describes the final one-click flow.
- [x] English installation manual describes the final one-click flow.
- [x] FLASHSHIP roadmap is current.
- [x] Audio / Sonus is marked `COMING SOON` unless real hardware testing is complete.
- [x] Credits are visible.
- [x] Disclaimer is visible.
- [x] Original third-party license texts remain unchanged.
- [x] Any Polish license translation is clearly marked informational/non-binding.

## Visuals

- [ ] Real `JRunner.MODI.exe` screenshot is present.
- [x] No test render is presented as a real running-session screenshot.
- [x] MODI logo is present.
- [x] HIGH SPEED → TURBO transition GIF is present.
- [x] Duplicate transition MP4 is removed from the GitHub product page/repository; keep MP4 for external video/social editing only.
- [x] GIF is reasonably optimized for web size.
- [x] Visual style matches MODI MAPS language but uses neon green / black / dark grey.

## Final hardware smoke test

Using the exact final public ZIP and `MODI-Setup.exe`:

- [x] start from a clean test folder / fresh-user scenario
- [x] installer obtains/detects compatible J-Runner 3.4.0.7 automatically or with one simple file selection
- [x] no compiler/SDK/source build occurs
- [x] ready `JRunner.MODI.exe` is created/installed
- [x] original `JRunner.exe` remains unchanged
- [x] MODI Flasher is detected
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

- [x] GitHub Release hashes match `SHA256SUMS.txt` exactly.
- [ ] Release notes list final Setup and firmware versions.
- [ ] Release notes link the exact corresponding firmware source.
- [ ] Changelog is updated.
- [ ] Direct download buttons point to the final public release assets.

## Current staging state — 2026-10-04

The frozen 0.9.0 draft remains as a baseline. The 0.9.1 candidate uses an offline compiled-IL patcher and one end-user ZIP. Exact clean-folder package checks pass. Final hardware smoke and genuine screenshot remain pending; firmware provenance review remains open.

## 0.9.1 Beta evidence (2026-10-04)

Exact final ZIP / Setup clean-folder check: PASS. Output SHA256: `8733FF2AD7852B0B2571C905F29E4CFBB0E1BC4BD17D924E8B95F04ABD0D73B4`. All 753 selected methods match donor IL; 18 offline integration checks pass. Original upstream executable and embedded third-party resource bytes stay unchanged. No compiler or source is extracted. One-click installation rejects unsupported originals, unknown existing MODI outputs and missing upstream support folders.

GIF lossless re-encode: 81/81 frames, pixels and timing identical, same 10,100,871-byte size; original retained. MP4 removed from main tree/product page, private source retained. Real screenshot remains pending after capture timeouts. Hardware READ/WRITE/readback/boot/repeat on the exact final package remains pending. Do not mark those hardware boxes from historical benchmark evidence.

Final GUI launch / MODI Turbo device detection: PASS. Release upload and all four GitHub asset SHA256 digests: PASS. READ/WRITE/readback/boot/repeat and genuine screenshot remain pending. Pages requires owner enablement; its token cannot create the site.
