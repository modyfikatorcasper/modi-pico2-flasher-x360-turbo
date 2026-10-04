# Release Checklist — MODI Pico 2 Flasher X360 TURBO

Use this checklist before publishing a public release.

## Files

- [ ] `MODI-Setup.exe` is the final tested build.
- [ ] `MODI-Pico2-Flasher-X360-TURBO.uf2` matches the documented firmware version.
- [ ] `SHA256SUMS.txt` contains hashes of every public binary.
- [ ] Matching GPL-compliant firmware source is available and linked.
- [ ] No full J-Runner package is included.
- [ ] No development workspace/source tree is included, except firmware source where legally required.
- [ ] No private dumps, CPU keys, customer files, build cache, SDK or NuGet cache are included.
- [ ] No third-party DLL with unclear redistribution rights is included.

## Documentation

- [ ] English README is current.
- [ ] Polish README is current.
- [ ] Polish installation manual is complete.
- [ ] English installation manual is complete.
- [ ] FLASHSHIP roadmap is current.
- [ ] Audio / Sonus is still marked `COMING SOON` unless real hardware testing is complete.
- [ ] Credits are visible.
- [ ] Disclaimer is visible.
- [ ] Original third-party license texts remain unchanged.
- [ ] Any Polish license translation is clearly marked informational/non-binding.

## Visuals

- [ ] Real `JRunner.MODI.exe` screenshot is present.
- [ ] No test render is presented as a real running-session screenshot.
- [ ] MODI logo is present.
- [ ] HIGH SPEED → TURBO transition GIF is present.
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

- [ ] Hardware benchmarks are clearly labelled as tested-hardware results.
- [ ] No installer benchmark claim is implied.
- [ ] No “world's fastest” claim unless backed by a public current comparison.
- [ ] Current safe wording is used: “one of the fastest low-cost Xbox 360 flashing solutions we have tested.”
- [ ] ~$5–6 wording clearly refers to the core development board only.

## Release integrity

- [ ] GitHub Release hash matches `SHA256SUMS.txt` exactly.
- [ ] Release notes list firmware and MODI Setup versions.
- [ ] Release notes link the exact corresponding firmware source.
- [ ] Changelog is updated.
