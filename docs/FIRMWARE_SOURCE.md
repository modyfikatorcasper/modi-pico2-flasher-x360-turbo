# Corresponding firmware source / Odpowiadające źródła firmware

Both files are public in [v0.9.1 Beta](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta):

- [TURBO UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2), SHA256 `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53`.
- [Matching source archive](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.1.zip), SHA256 `042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8`.

The archive contains the complete firmware C/header/PIO/CMake inputs, original GPL license texts, unchanged Pico SDK 2.1.0 and TinyUSB sources with license texts, source hashes and BUILD.md. Compiler binaries, caches, J-Runner sources and private service data are excluded. The source inputs match the preserved build; a byte-identical rebuild in a different directory/toolchain is not asserted.

PL: Źródła firmware są osobnym, publicznym archiwum. Zawierają komplet plików firmware, źródła SDK/TinyUSB, oryginalne licencje i instrukcję budowania. UF2 oraz odpowiadające źródła są dostępne bez dodatkowej opłaty w tym samym wydaniu. Nie publikujemy pełnych źródeł J-Runnera.

License status / Licencje: inherited headers specify GPLv2; inherited LICENSE contains GPLv3. Both are preserved without relicensing; upstream provenance review remains open. See LICENSE-VERSION-NOTICE.md in the archive.
