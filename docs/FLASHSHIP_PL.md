# MODI X360 ULTIMATE — moduły serwisowe

[English](FLASHSHIP.md)

**ULTIMATE PREVIEW / IN DEVELOPMENT.** TURBO pozostaje sprawdzonym modułem flashowania. ULTIMATE rozwija go w docelową platformę serwisową: backup, RGH, CPU Key, Audio/Sonus, programowanie chipów, LIVE i konwersje pamięci.

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

Jedno urządzenie, jeden docelowy header serwisowy, jeden program i kolejne tryby pracy. Nie wszystkie operacje równocześnie. Istniejący header NAND GP0–GP5 nie zawiera dodatkowych pinów Audio/JTAG/LIVE; wspólny header wymaga ich wyprowadzenia zgodnie z mapą.

[ULTIMATE](ULTIMATE_PL.md) · [Conversions](CONVERSIONS_PL.md) · [Wiring](FLASHSHIP_WIRING_PL.md) · [Pre-final](PRE_FINAL_PL.md) · [Alpha](ALPHA_PL.md)


