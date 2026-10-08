# MODI X360 ULTIMATE — pre-final / Alpha

[English](PRE_FINAL.md) · [ULTIMATE](ULTIMATE_PL.md)

**ULTIMATE PREVIEW / IN DEVELOPMENT — 2026-10-08**

Kanał Stable zachowuje sprawdzone binaria TURBO v0.9.1-beta. Kanał Alpha udostępnia odrębne profile preview i ich odpowiadające źródła. Nazwa, pliki i tag wcześniejszego v0.9.1-beta pozostają zachowane.

| Module | Status | Zakres |
|---|---|---|
| TURBO NAND / eMMC | **TESTED** | Sprawdzony zakres NAND/eMMC. Binaria i czasy bez zmian. |
| Audio / Sonus | **PREVIEW · HARDWARE VALIDATION PENDING** | Cyfrowe ISD2100. MODI RDY = GP22. |
| UART / COM Monitor | **PREVIEW · HARDWARE VALIDATION PENDING** | Odbiór na żywo, logi i komunikaty głosowe. |
| XeLL CPU Key Assistant | **PREVIEW** | Obecny panel LAN; docelowe przechwycenie przez UART/LIVE w rozwoju. |
| HANA / SMBus LIVE Monitor | **PREVIEW · HARDWARE VALIDATION PENDING** | Pasywny nasłuch SMBus. Pełna diagnostyka HDMI wymaga osobnej walidacji. |
| Automatic RGH Assistant | **IN DEVELOPMENT** | Plan jednego workflow z dwoma backupami i odczytem kontrolnym. |
| Memory Conversions | **IN DEVELOPMENT** | Planowane obrazy pod fizyczną wymianę układu pamięci na NAND 16 MB. |
| Xbox 360 DVD Remarry | **RESEARCH** | Przyszły moduł badawczy; brak funkcji remarry w obecnym firmware. |

**Stan obecny:** jeden Pico uruchamia jeden profil UF2. Audio, MODI Chip Flasher, UART oraz LIVE są oddzielnymi buildami. LIVE może odbierać UART i SMBus jednocześnie; nie łączy to wszystkich trybów flashowania. Automatyczne przełączanie trybów w jednym firmware i jeden wspólny program są celem rozwoju.

Pełny lokalny JRunner LIVE preview nie jest dołączany do publicznej paczki. Alpha zawiera własny panel MODI-Flashship dla Audio, MODI Chip Flasher, osobnego UART i XeLL LAN; surowy profil LIVE wymaga zgodnego hosta MLIV z lokalnego developmentu. Publiczny updater łączący te tryby z J-Runnerem pozostaje do dopięcia.

Nie kompilowano ponownie sprawdzonego TURBO ani Setup. Alpha pakuje istniejące buildy profili; nie jest nowym wspólnym firmware. Nie wykonano nowego testu sprzętowego podczas przygotowania wydania.

## Wymagania 1.0

Przed 1.0: wspólny firmware i bezpieczne przełączanie trybów; publiczny updater hosta; testy sprzętowe Audio (ID/backup/write/readback/play), JTAG (IDCODE/program/verify), UART i jednoczesnego SMBus; walidacja CPU Key i pełnego RGH; każda kombinacja konwersji z odczytem kontrolnym i startem konsoli; własne fotografie; testy telefonu/PL/EN; zgodność źródeł i licencji. DVD Remarry pozostaje badaniem poza obietnicą 1.0.

[Conversions](CONVERSIONS_PL.md) · [Wiring](FLASHSHIP_WIRING_PL.md) · [Alpha instructions](ALPHA_PL.md)

Paczka SOURCE zawiera wyłącznie wymagane źródła firmware i dependencies z licencjami. Prywatne źródła Setup, JRunner.MODI i aplikacji MODI pozostają niepubliczne.

