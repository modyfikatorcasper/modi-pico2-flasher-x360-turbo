# MODI X360 ULTIMATE Alpha 1 — 1.0.0-alpha.1

[English](ALPHA.md) · [ULTIMATE](ULTIMATE_PL.md)

**ALPHA / PREVIEW · HARDWARE VALIDATION PENDING**

To paczka istniejących buildów z 5 października 2026, opublikowana 8 października. Nie jest nowym wspólnym firmware ULTIMATE. Stable zachowuje sprawdzony TURBO.

## Instalacja

1. Pobierz kompletny ZIP Alpha, rozpakuj i uruchom MODI-Flashship.exe. Windows / .NET Framework 4.8. MODI-Setup.exe pozostaje instalatorem stabilnego TURBO do zgodnej własnej instalacji J-Runnera.
2. W BOOTSEL wgraj jeden profil z tabeli. Nie kopiuj wszystkich UF2 jednocześnie. Zamknij aplikację zajmującą COM przed uruchomieniem innego narzędzia.
3. Podłącz według diagramu właściwego modułu. Audio RDY = GP22, GP11 = pasywny SMB_DATA. Logika 3,3 V; wspólna masa.
4. Do NAND/eMMC przywróć TURBO. Alpha nie zmienia sprawdzonych timingów NAND/eMMC.

| Profil | Host / zakres |
|---|---|
| MODI-Pico2-Flasher-X360-TURBO.uf2 | JRunner.MODI ze Stable; NAND/eMMC |
| MODI-Audio-Sonus-PREVIEW.uf2 | MODI-Flashship → Audio / Sonus; GP12–15, **RDY GP22** |
| MODI-DirtyJTAG-PREVIEW.uf2 | MODI-Flashship → MODI Chip Flasher; GP16–19; helper xsvftool i sterownik z własnej instalacji |
| MODI-UART-MONITOR-PREVIEW.uf2 | MODI-Flashship → COM / UART; MUAR; GP9 RX |
| MODI-LIVE-UART-HANA-PREVIEW.uf2 | Zaawansowany profil UART+SMBus; wymaga hosta MLIV z lokalnego preview, którego ten publiczny ZIP nie zawiera |

Główny plik do pobrania MODI-X360-ULTIMATE-UART-ALPHA.uf2 ma dokładnie te same bajty co profil MODI-UART-MONITOR-PREVIEW.uf2. Obsługuje tylko nasłuch UART, nie cały zestaw ULTIMATE.


XeLL LAN pozostaje osobnym panelem programu. Automatyczny RGH, CPU Key przez UART/LIVE, konwersje pamięci i DVD Remarry są w rozwoju. Pasywny nasłuch SMBus nie jest pełnym testem HDMI.

## Testy i źródła

Testy offline własnego panelu zakończyły się kodem 0; sprawdzono struktury UF2, CRC ZIP i hashe. To nie jest test sprzętowy. Audio, JTAG, UART i SMBus wymagają fizycznej walidacji. Jedno archiwum SOURCE zawiera odpowiadające źródła wszystkich pięciu profili i wymagane dependencies/licencje. Nie zawiera prywatnych źródeł aplikacji.

[Wiring](FLASHSHIP_WIRING_PL.md) · [Photo credits](PHOTO-CREDITS.md)

