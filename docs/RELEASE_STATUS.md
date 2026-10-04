# Release status — 0.9.0 Beta

Binaries were prepared from the preserved baseline without recompilation or transport changes. The GitHub Release is being prepared as a **draft**, not a final 1.0 release. Public material here is documentation and branding.

Pending: exact installer → device detection → READ → known-good WRITE → physical READ BACK/compare → console boot → another operation without restarting J-Runner. A genuine screenshot remains pending after two capture-tool timeouts. No new hardware tests were performed in this step.

| File | Bytes | SHA256 |
|---|---:|---|
| `MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.0.zip` | 6,510,302 | `042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8` |
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | 92,160 | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Setup.exe` | 1,957,376 | `61CC8E46CFB7EBB5C96B0B5AEE93EA1EB5743FB7646024B6FFCA9B5F5042331E` |
| `SHA256SUMS.txt` | 312 | `D7DB11FF8FAB818CF7A362A6E9B8D69E99D62840015BED93889E725F16281EA4` |

[Firmware source](FIRMWARE_SOURCE.md) · [Checklist](../RELEASE-CHECKLIST.md).

Setup retains its embedded MIT/MODI patch required for local building. Separate J-Runner sources and a full package are not published. GPL firmware corresponding source is a separate archive with licenses and build instructions.

License status / Licencje: inherited headers specify GPLv2; inherited LICENSE contains GPLv3. Both are preserved, without relicensing. Upstream provenance review remains open before final firmware publication. See the source archive LICENSE-VERSION-NOTICE.md.
