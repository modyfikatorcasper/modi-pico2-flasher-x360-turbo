# Release status — 0.9.1 Beta (draft)

Offline one-click patcher and one end-user ZIP are prepared. Tested from a fresh folder with Unicode/spaces: pinned upstream verification, automatic copy patching, original preservation, repeat installation, incompatible original rejection, unknown existing output preservation and missing support-folder rejection.

The exact Setup-produced application passes 753 donor method comparisons and 18 offline integration checks. Protected upstream code and original embedded third-party DLL resources are preserved. No hardware operation was run on this exact final package.

| File | Bytes | SHA256 |
|---|---:|---|
| `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip` | 2,851,168 | `BCE31A9EE63BBB1AE9AD601A472C64E6928BFC5701D1BBE6C0A95455A67D5B16` |
| `MODI-Setup.exe` | 3,001,344 | `40EC3430563DA2FC5B261A8D2BC3F62E6684D9CCB02453A2FFCCA03420CA2C2D` |
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | 92,160 | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.1.zip` | 6,510,302 | `042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8` |

The frozen firmware is unchanged (same UF2 and source bytes as 0.9.0). Installation remains dependent on the user's complete pinned J-Runner 3.4.0.7 installation. No full J-Runner, separate application source, or unclear external DLL is bundled.

Pending: exact ZIP → Setup → device detect → READ → known-good WRITE → physical READ BACK/compare → console boot → another operation without restart. Genuine window capture is pending because the capture helper returned FrameArrived timeout and window capture timeout. No test render is substituted. The GIF passed an exact 81-frame pixel/timing check; lossless re-encoding gave no size reduction, so the original is retained. MP4 is excluded from this repository, with the local original retained privately.

Inherited firmware GPLv2 header / GPLv3 LICENSE provenance review remains open. Both original texts remain included. This is a draft Beta, not a final Stable release.

[Distribution audit](DISTRIBUTION_AUDIT.md) · [Matching firmware source](FIRMWARE_SOURCE.md) · [Checklist](../RELEASE-CHECKLIST.md).

Audio/Sonus: COMING SOON. DirtyJTAG/UART: PLANNED. HANA: RESEARCH. Upstream: PROPOSED.
