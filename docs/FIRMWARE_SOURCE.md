# Corresponding firmware source / Odpowiadające źródła firmware

Candidate: `MODI-Pico2-Flasher-X360-TURBO.uf2`, SHA256
`FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53`.

The matching archive is `MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.0.zip`, SHA256
`042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8`.

It contains the complete firmware C/header/PIO/CMake inputs, original GPL license texts,
unchanged Pico SDK 2.1.0 and TinyUSB sources with license texts, source hashes,
and BUILD.md (configuration and installation instructions). General-purpose
compiler binaries, caches, J-Runner sources and private service data are excluded.
The source inputs match the preserved build; a byte-identical rebuild in a
different directory/toolchain is not asserted.

Both UF2 and its source archive are staged together in the matching
[GitHub Release](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases).
A draft release is visible only to maintainers. Neither download is announced
as publicly available until that draft is published. Whenever UF2 is published,
the matching source archive must be published alongside it at no extra charge.

PL: Źródła są osobnym archiwum wymaganym dla firmware GPL. Zawierają komplet
wejść firmware, źródła SDK/TinyUSB, oryginalne licencje i instrukcję budowania.
UF2 oraz archiwum źródłowe udostępniamy razem w tym samym wydaniu. Draft jest
widoczny tylko dla opiekunów repo. Nie ogłaszamy tych plików jako publicznie
dostępnych przed publikacją draftu. Nie publikujemy pełnych źródeł J-Runnera.

License status / Licencje: inherited headers specify GPLv2; inherited LICENSE contains GPLv3. Both are preserved, without relicensing. Upstream provenance review remains open before final firmware publication. See the source archive LICENSE-VERSION-NOTICE.md.
