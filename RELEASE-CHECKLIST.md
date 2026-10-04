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
- [x] Complete matching firmware source and original license texts are public and linked; inherited license-version provenance review remains open.
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
- [x] READ succeeds — user-reported completion
- [x] dump is correct / expected comparison succeeds — user-reported completion
- [x] WRITE known-good image succeeds — user-reported completion
- [x] READ BACK / binary compare succeeds — user-reported completion
- [x] console boots — user-reported completion
- [x] another operation can start without restarting J-Runner — user-reported completion

## Claims

- [x] Hardware benchmarks are clearly labelled as tested-hardware results.
- [x] No installer benchmark claim is implied.
- [x] No “world's fastest” claim unless backed by a public current comparison.
- [x] Current safe wording is used: “one of the fastest low-cost Xbox 360 flashing solutions we have tested.”
- [x] ~$5–6 wording clearly refers to the core development board only.

## Release integrity

- [x] GitHub Release hashes match `SHA256SUMS.txt` exactly.
- [x] Release notes list final Setup and firmware versions.
- [x] Release notes link the exact corresponding firmware source.
- [x] Changelog is updated.
- [x] Direct download buttons point to the final public release assets.

## Public release evidence — 2026-10-04

0.9.1 Beta is public. The frozen 0.9.0 draft remains a baseline. Setup and firmware bytes are unchanged; ZIP instructions now link the official pinned upstream base. Exact hashes are in SHA256SUMS.txt and docs/RELEASE_STATUS.md.

Exact clean-folder installation: PASS. Output SHA256: `8733FF2AD7852B0B2571C905F29E4CFBB0E1BC4BD17D924E8B95F04ABD0D73B4`. All 753 selected methods match donor IL; 18 offline integration checks pass. Unsupported originals, unknown existing outputs and missing support folders are rejected. Actual final application launch and MODI Turbo detection: PASS.

Hardware checkboxes above record the user's 2026-10-04 reply to the final test request: “TEST SA WYKONA WSZYSTKO DZIALA”. This is a general user confirmation of completed tests, not an agent-observed new measurement or supplied per-step log. Historical timings are not reused as new QA.

Release publication and all binary/archive digests: PASS (run 37224245574). Official upstream r7 executable matches the installer pin. GitHub Pages deployment: PASS (run 37224245466).

GIF check: 81 identical frames and durations; original retained. MP4 removed from main/product page. Genuine screenshot remains pending after capture timeouts; no render is substituted. Inherited firmware license-version provenance review remains open.

## Clean four-asset distribution — 2026-10-04

- [x] Exactly UF2, installation ZIP, one SOURCE ZIP and SHA256SUMS.txt are allowed by publication workflow.
- [x] Standalone Setup and license/notice assets are removed after the matching SOURCE ZIP is uploaded and hash-verified.
- [x] Setup and UF2 bytes are unchanged; firmware source and original dependency source archives are preserved byte-for-byte.
- [x] Installation ZIP contains binaries, START-HERE PL/EN, internal hashes and required notices; no development source/scripts/SDK/debug files.
- [x] SOURCE ZIP contains firmware inputs, required source dependencies, build instructions and original notices; no application/integration source.
- [x] README and Pages use UF2 → complete package → manual; source compliance has a small footer link.
- [x] Obsolete staging workflow using a wildcard is removed; publication uses an explicit four-file allowlist.
