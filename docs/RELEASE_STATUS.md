# Release status — 0.9.1 Beta (public)

Offline one-click patcher and one end-user ZIP are prepared. Tested from a fresh folder with Unicode/spaces: pinned upstream verification, automatic copy patching, original preservation, repeat installation, incompatible original rejection, unknown existing output preservation and missing support-folder rejection.

The exact Setup-produced application passes 753 donor method comparisons and 18 offline integration checks. Protected upstream code and original embedded third-party DLL resources are preserved. The final application launches and identifies the attached Pico as MODI Turbo. The user confirmed successful hardware tests on 2026-10-04: “TEST SA WYKONA WSZYSTKO DZIALA”. This is user-reported completion, without new per-operation measurements or readback hashes.

| File | Bytes | SHA256 |
|---|---:|---|
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | 92,160 | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip` | 3,245,306 | `E18BF9E6EAD0353842920D88362749FD1B4F5FFE8976DD11ADE7A37151240D53` |
| `MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip` | 8,133,110 | `9E26CB674949012C1C9B9E65BB68E91EE3FB98F4955EC90549143C9513A407D4` |
| `SHA256SUMS.txt` | 326 | `26089A402C0BF5877EBD56052ECE53E440B942939F7E8E99F162A6B0971DA181` |

The frozen firmware is unchanged (same UF2 and source bytes as 0.9.0). Installation remains dependent on the user's complete pinned J-Runner 3.4.0.7 installation. No full J-Runner, separate application source, or unclear external DLL is bundled.

Genuine window capture is pending because the capture helper returned FrameArrived timeout and window capture timeout. No test render is substituted. The GIF passed an exact 81-frame pixel/timing check; lossless re-encoding gave no size reduction, so the original is retained. MP4 is excluded from this repository, with the local original retained privately.

The [public v0.9.1-beta release](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta) is available. Publication workflow 37224245574 passed, including the exact ZIP and asset digests and a fresh download of the official upstream r7 archive whose executable matches the installer pin. All four release asset digests match the table above. [GitHub Pages](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/) deployment succeeded in run 37224245466.

Inherited firmware GPLv2 header / GPLv3 LICENSE provenance review remains open. Both original texts remain included. This is a public Beta, not a final Stable release.

[Distribution audit](DISTRIBUTION_AUDIT.md) · [Matching firmware source](FIRMWARE_SOURCE.md) · [Checklist](../RELEASE-CHECKLIST.md).

## Clean release layout

Exactly four assets are published, ordered in the description as UF2, complete installation ZIP, one SOURCE ZIP and SHA256SUMS.txt. Standalone Setup and license assets are removed. Setup stays inside the installation ZIP with unchanged SHA256 `40EC3430563DA2FC5B261A8D2BC3F62E6684D9CCB02453A2FFCCA03420CA2C2D`. Firmware inputs and dependency source archives are preserved byte-for-byte inside the reorganized SOURCE ZIP. No binary compilation, NAND/eMMC changes or timing changes were performed.
