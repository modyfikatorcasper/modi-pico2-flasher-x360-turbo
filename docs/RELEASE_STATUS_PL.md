# Stan wydania 0.9.0 Beta

Binaria przygotowano z zachowanej bazy, bez ponownej kompilacji i bez zmiany transportu. Wydanie na GitHubie jest przygotowywane jako **draft**, nie jako finalne 1.0. Widoczne publicznie materiały są dokumentacją i brandingiem.

Otwarte: końcowy test dokładnego instalatora → wykrycie → READ → zapis sprawdzonego obrazu → fizyczny READ BACK/compare → boot konsoli → kolejna operacja bez restartu J-Runnera. Prawdziwy screenshot jest otwarty, ponieważ narzędzie przechwytywania dwukrotnie zwróciło timeout. Brak nowych testów sprzętowych w tym kroku.

| File | Bytes | SHA256 |
|---|---:|---|
| `MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.0.zip` | 6,510,302 | `042CAC51B051FD565C6AAAB0629FA50098E2082A01972BCE74746BDD9A84FFE8` |
| `MODI-Pico2-Flasher-X360-TURBO.uf2` | 92,160 | `FAFACB8FDF912B9B335013B7B653942A347564DF5A9AB62D1BBE895BDCCBDD53` |
| `MODI-Setup.exe` | 1,957,376 | `61CC8E46CFB7EBB5C96B0B5AEE93EA1EB5743FB7646024B6FFCA9B5F5042331E` |
| `SHA256SUMS.txt` | 312 | `D7DB11FF8FAB818CF7A362A6E9B8D69E99D62840015BED93889E725F16281EA4` |

[Źródła firmware](FIRMWARE_SOURCE.md) · [Checklist](../RELEASE-CHECKLIST.md).

Setup zawiera tylko osadzony patch MIT/MODI potrzebny do lokalnego budowania. Nie publikujemy osobnych źródeł J-Runnera ani pełnego pakietu. Odpowiadające źródła GPL firmware są osobnym archiwum z licencjami i instrukcją budowania.

License status / Licencje: inherited headers specify GPLv2; inherited LICENSE contains GPLv3. Both are preserved, without relicensing. Upstream provenance review remains open before final firmware publication. See the source archive LICENSE-VERSION-NOTICE.md.
