# MODI X360 ULTIMATE — podłączenia preview

[English](FLASHSHIP_WIRING.md) · [Status pre-final](PRE_FINAL_PL.md) · [NAND i eMMC](WIRING_PL.md)

Te połączenia dotyczą nowych profili preview. Audio, MODI Chip Flasher i LIVE wymagają testów sprzętowych. Jeden Pico ma w tej wersji jeden aktywny profil UF2. Do NAND/eMMC wróć do sprawdzonego TURBO.

Kolory nowych diagramów są pomocnicze. Nie określają kolorów istniejącego kabla NAND GP0–GP5. Fotografie pokazują wybrane rewizje sprzętu z zaznaczonymi padami. Osobne schematy SVG pokazują sygnały; nie odwzorowują fizycznych odległości ani układu padów wszystkich rewizji. Sprawdź oznaczenia na swojej płycie przed lutowaniem.

## Header RP2350 Plus

![Dodatkowe piny Audio JTAG i LIVE](../assets/wiring/photo-flashship-header.png)

[Schemat sygnałów](../assets/wiring/wiring-flashship-header-rp2350-plus.svg)

Widok tyłu, USB u góry. Audio korzysta z GP12–GP15 i GP22, MODI Chip Flasher z GP16–GP19. GP20 i GP21 są opcjonalnymi resetami. LIVE używa GP9–GP11 jako wejść. Wspólna masa jest wymagana. GPIO pracują z logiką 3,3 V; nie podłączaj 5 V ani RS-232. Zasilanie układu docelowego zapewnij zgodnie z jego dokumentacją.

## Audio Sonus w Trinity i Corona

Profil `MODI-Audio-Sonus-PREVIEW.uf2` obsługuje cyfrowe ISD2100. Nie dotyczy analogowej rodziny ISD1200 z logiką 5 V.

| Sygnał | MODI GPIO | Trinity | Corona |
|---|---|---|---|
| MISO | GP12 | FT2R7 | J2C2-B11 |
| SSB / CS_N | GP13 | FT2R6 | J2C2-A11 |
| SCLK | GP14 | FT2T4 | J2C2-A8 |
| MOSI | GP15 | FT2T5 | J2C2-B8 |
| RDY / BSYB | **GP22** | FT2V4 | J2C2-A10 |
| GND | GND | zweryfikowana masa płyty | zweryfikowana masa płyty |

**W MODI RDY jest na GP22.** Oryginalna tabela X360Tools używa GP11; ten pin w MODI jest przeznaczony na pasywny nasłuch SMB_DATA.

![Audio Trinity](../assets/wiring/photo-audio-trinity.png)

[Schemat sygnałów](../assets/wiring/wiring-audio-trinity-rp2350-plus.svg)

![Audio Corona](../assets/wiring/photo-audio-corona.png)

[Schemat sygnałów](../assets/wiring/wiring-audio-corona-rp2350-plus.svg)

Oznaczenia punktów pochodzą z [tabeli Audio/Sonus autora PicoFlashera](https://github.com/X360Tools/PicoFlasher/blob/master/README.md). GP22 wynika z naszego firmware. Przed pierwszym zapisem wykonaj dwa pełne odczyty układu Audio, porównaj je i zachowaj kopię. PLAY zależy od indeksów głosów zapisanych w obrazie.

## MODI Chip Flasher — programator chipów

Profil `MODI-DirtyJTAG-PREVIEW.uf2` korzysta z istniejącego w instalacji użytkownika `xsvftool-dirtyjtag.exe`. Obsługuje ścieżkę SVF/XSVF. Zacznij od 100 kHz i stabilnego IDCODE; dobierz plik timingów do konkretnego modelu i rewizji.

| GPIO MODI | Sygnał na chipie | Kierunek |
|---|---|---|
| GP16 | TDI | Pico → chip |
| GP17 | TDO | chip → Pico |
| GP18 | TCK | Pico → chip |
| GP19 | TMS | Pico → chip |
| GND | GND | wspólna masa |
| GP20 | SRST | tylko jeżeli wymagany |
| GP21 | TRST | tylko jeżeli wymagany |

VCC nie jest pinem GPIO. Chip zasilaj osobno zgodnie z jego instrukcją. Nie przenoś fizycznej kolejności padów między rewizjami.

### X360ACE V3

![ACE V3](../assets/wiring/photo-dirtyjtag-ace-v3.png)

[Schemat sygnałów](../assets/wiring/wiring-dirtyjtag-ace-v3-rp2350-plus.svg)

### CoolRunner

![CoolRunner](../assets/wiring/photo-dirtyjtag-coolrunner.png)

[Schemat sygnałów](../assets/wiring/wiring-dirtyjtag-coolrunner-rp2350-plus.svg)

Ustaw PRG na wariantach z przełącznikiem programowania.

### Matrix Glitcher

![Matrix](../assets/wiring/photo-dirtyjtag-matrix.png)

[Schemat sygnałów](../assets/wiring/wiring-dirtyjtag-matrix-rp2350-plus.svg)

Podłącz według napisów TDI/TDO/TCK/TMS/GND. Schemat nie deklaruje wspólnej kolejności fizycznych padów dla wszystkich Matrixów.


## Pliki do druku

Otwórz zdjęcie powyżej w pełnym rozmiarze, aby powiększyć lub wydrukować. SVG można powiększać bez utraty ostrości. Zbliżenia powyżej zawierają kadry zdjęć sprzętu i oznaczenia MODI. PDF oraz osobne SVG zawierają schematy sygnałów. [Źródła fotografii i autorzy](PHOTO-CREDITS.md).

## Docelowe mapy MODI

Obecne fotografie referencyjne są tymczasowe; zachowujemy autorów i oznaczenia. Potrzebujemy własnych zdjęć MODI: całych płyt Corona (osobno rewizje), Trinity i Fat; makro padów Audio, UART/SMBus i punktów konwersji; przodu/tyłu chipów ACE, CoolRunner i Matrix; RP2350 Plus z kompletnym headerem. Docelowy układ: **lewa — pełna płyta z lokalizacją; środek — makro padów; prawa — rzeczywisty Pico z GPIO**. Na grafikach krótkie nazwy sygnałów, opisy PL/EN pod spodem; na telefonie pojedyncza kolumna i powiększenie.

Jedno urządzenie, jeden docelowy header serwisowy, jeden program i kolejne tryby pracy. Nie wszystkie operacje równocześnie. Istniejący header NAND GP0–GP5 nie zawiera dodatkowych pinów Audio/JTAG/LIVE; wspólny header wymaga ich wyprowadzenia zgodnie z mapą.

[ULTIMATE](ULTIMATE_PL.md) · [Alpha](ALPHA_PL.md)

