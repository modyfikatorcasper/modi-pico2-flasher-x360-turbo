# MODI X360 ULTIMATE — All-in-One Xbox 360 Service Tool

[English](ULTIMATE.md) · [TURBO](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta) · [Alpha](ALPHA_PL.md)

**ULTIMATE PREVIEW / IN DEVELOPMENT**

[Główne ustalenia FLASHSHIP / ULTIMATE](PROJECT-AGREEMENTS_PL.md) · [DEVLOG / LAB NOTES](DEVLOG_PL.md)

**MODI FLASHSHIP = sprzęt RP2350 (FLASH + FLAGSHIP). MODI X360 ULTIMATE = cały docelowy system. TURBO = moduł NAND/eMMC.**

![MODI X360 ULTIMATE](../assets/logo/modi-x360-ultimate-transparent.png)

TURBO pozostaje sprawdzonym modułem flashowania. ULTIMATE rozwija go w docelową platformę serwisową: backup, RGH, CPU Key, Audio/Sonus, programowanie chipów, LIVE i konwersje pamięci.

**ONE DEVICE. ONE HEADER. ONE SOFTWARE. FULL XBOX 360 SERVICE WORKFLOW.**

Jedno urządzenie, jeden docelowy header serwisowy, jeden program i kolejne tryby pracy. Nie wszystkie operacje równocześnie. Istniejący header NAND GP0–GP5 nie zawiera dodatkowych pinów Audio/JTAG/LIVE; wspólny header wymaga ich wyprowadzenia zgodnie z mapą.

**Stan obecny:** jeden Pico uruchamia jeden profil UF2. Audio, MODI Chip Flasher, UART oraz LIVE są oddzielnymi buildami. LIVE może odbierać UART i SMBus jednocześnie; nie łączy to wszystkich trybów flashowania. Automatyczne przełączanie trybów w jednym firmware i jeden wspólny program są celem rozwoju.

## Moduły i status

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

## Automatic RGH Assistant — IN DEVELOPMENT

`CONNECT → READ #1 → READ #2 → COMPARE → CREATE XeLL → WRITE XeLL → BOOT → CAPTURE CPU KEY → BUILD IMAGE → WRITE → READBACK VERIFY → DONE`

**Docelowo:** bez telewizora, ręcznego IP ani wymaganego LAN do przechwycenia CPU Key. Program ma odebrać klucz przez obsługiwany COM/UART/LIVE, sprawdzić go względem danych konsoli i zapisać lokalnie. To plan, nie potwierdzona obsługa wszystkich rewizji: trzeba potwierdzić wyjście danych XeLL, baud, połączenia i parser klucza. Panel XeLL LAN pozostaje alternatywą preview. Sama aktywność SMBus/HANA nie ujawnia CPU Key.

## Audio / Sonus

**MODI Audio RDY = GP22. GP11 = passive SMB_DATA.** GP12 MISO, GP13 CS, GP14 CLK, GP15 MOSI, GND. [Wiring](FLASHSHIP_WIRING_PL.md). Digital ISD2100; analog ISD1200 5 V is not supported.

## HANA / SMBus LIVE Monitor

Nazwą obecnego modułu jest **HANA / SMBus LIVE Monitor**. Docelowy panel może pokazywać NO ACTIVITY, SMBus ACTIVITY, HANA ACTIVITY DETECTED lub BOOT STAGE REACHED dopiero po potwierdzeniu reguł interpretacji. Pasywne dane z magistrali nie potwierdzają obrazu, HDCP, HDMI ani sprawności HANA.

## ULTIMATE MEMORY CONVERSIONS — IN DEVELOPMENT

[Pełny plan konwersji i rewizje](CONVERSIONS_PL.md)

## Koncepcja UI

Koncepcja ekranu na stronie nie jest działającym programem. CONSOLE DETECTED będzie widoczne dopiero po rozpoznaniu urządzenia. Duże tryby: BACKUP / RESTORE, AUTOMATIC RGH, MEMORY CONVERSION, GLITCH CHIP PROGRAMMER, AUDIO / SONUS, LIVE MONITOR, HANA DIAGNOSTICS i RECOVERY. Rozpoznanie rewizji/geometrii ma ograniczać ręczne ustawienia; niepewne dane zatrzymują zapis. HANA DIAGNOSTICS jest docelową nazwą UI, nie deklaracją pełnego testu HDMI.

## Fotografie i wiring

Obecne fotografie referencyjne są tymczasowe; zachowujemy autorów i oznaczenia. Potrzebujemy własnych zdjęć MODI: całych płyt Corona (osobno rewizje), Trinity i Fat; makro padów Audio, UART/SMBus i punktów konwersji; przodu/tyłu chipów ACE, CoolRunner i Matrix; RP2350 Plus z kompletnym headerem. Docelowy układ: **lewa — pełna płyta z lokalizacją; środek — makro padów; prawa — rzeczywisty Pico z GPIO**. Na grafikach krótkie nazwy sygnałów, opisy PL/EN pod spodem; na telefonie pojedyncza kolumna i powiększenie.

[Źródła obecnych zdjęć](PHOTO-CREDITS.md)

## Przed ULTIMATE 1.0

Przed 1.0: wspólny firmware i bezpieczne przełączanie trybów; publiczny updater hosta; testy sprzętowe Audio (ID/backup/write/readback/play), JTAG (IDCODE/program/verify), UART i jednoczesnego SMBus; walidacja CPU Key i pełnego RGH; każda kombinacja konwersji z odczytem kontrolnym i startem konsoli; własne fotografie; testy telefonu/PL/EN; zgodność źródeł i licencji. DVD Remarry pozostaje badaniem poza obietnicą 1.0.

Optional native upstream J-Runner support remains a proposal without implied endorsement.

