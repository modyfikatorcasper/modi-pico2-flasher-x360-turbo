# MODI Pico 2 Flasher X360 TURBO

**Szybki i tani programator NAND i eMMC dla Xbox 360 na RP2350 / Pico 2 z integracją J-Runner.**  
Diagramy Corona, Trinity i Fat. Jeden header MODI. Jeden workflow SPI. Stable TURBO.

**🇵🇱 Polski** · [🇬🇧 English](README.md)

[![Otwórz MODI Pico 2 Flasher X360 TURBO](assets/buttons/open-modi-flasher.svg)](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/)

## Tożsamość projektu

**Kacper Lewandowski — GitHub: `modyfikatorcasper`, znany również jako Modyfikator89, Modyfikator Kacper i Modi.**  
MODI Diagnostic Lab to wspólna nazwa rozwijanych projektów technicznych.

## Pobierz

**[POBIERZ UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO.uf2)**  
[POBIERZ PEŁNĄ PACZKĘ](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip)  
[OTWÓRZ STRONĘ PROJEKTU](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/) · [INSTRUKCJA](docs/INSTALL_PL.md) · [OKABLOWANIE](docs/WIRING_PL.md)

![MODI Pico 2 Flasher X360 TURBO](assets/logo/modi-turbo.png)

## Programator Xbox 360 stworzony do szybkiego serwisu

**MODI Pico 2 Flasher X360 TURBO** to niezależny programator serwisowy NAND i eMMC dla Xbox 360 oparty na niedrogim sprzęcie **RP2350 / Pico 2**.

Powstał do napraw konsol, backupu NAND, odzyskiwania pamięci oraz pracy przy RGH. Workflow ma być prosty: wgrywasz UF2, uruchamiasz gotową paczkę, podłączasz flasher i korzystasz z integracji MODI w J-Runnerze.

### Potwierdzone wyniki sprzętowe

| Pamięć / testowany zakres | READ | WRITE |
|---|---:|---:|
| NAND 16 MB | ~19 s | ~24 s |
| Jasper Big Block, testowany zakres 64 MiB + spare | 76.890–76.955 s | 90.171 s |
| Corona eMMC, testowany zakres 48 MiB | 56.198–57.792 s | 48.310 s |

Wyniki pochodzą z testowanego sprzętu. Rzeczywiste czasy mogą się różnić zależnie od rewizji płyty, jakości połączeń, hosta USB i konfiguracji systemu.

Na obecnym etapie opisujemy MODI jako **jedno z najszybszych tanich rozwiązań do flashowania Xbox 360, jakie przetestowaliśmy**. Do bezwzględnego hasła „najszybszy na świecie” potrzebne byłoby szersze publiczne porównanie.

## Jeden header. Jeden workflow SPI.

Po stronie MODI układ przewodów pozostaje spójny dla obsługiwanych diagramów Xbox 360.

**GP0 = SPI_MISO**  
**GP1 = SPI_SS_N**  
**GP2 = SPI_CLK**  
**GP3 = SPI_MOSI**  
**GP4 = SMC_DBG_EN**  
**GP5 = SMC_RST_XDK_N**  
**GND = GND**

Na naszym siedmiopozycyjnym headerze RP2350-Plus, patrząc od USB w dół:

**pomarańczowy GP0 → brązowy GP1 → żółty GND → czerwony GP2 → czarny GP3 → niebieski GP4 → zielony GP5**

Diagramy połączeń:

- [Corona](assets/wiring/wiring-corona-rp2350-plus.png)
- [Trinity](assets/wiring/wiring-trinity-rp2350-plus.png)
- [Falcon / Fat](assets/wiring/wiring-falcon-rp2350-plus.png)
- [Pełny manual okablowania](docs/WIRING_PL.md)

Przed podłączeniem zawsze sprawdź rewizję płyty i właściwe punkty lutownicze.

## Szybki start

1. Pobierz `MODI-Pico2-Flasher-X360-TURBO.uf2` albo pełną paczkę wydania.
2. Uruchom Pico 2 / RP2350 w trybie **BOOTSEL** i skopiuj UF2.
3. Podłącz flasher zgodnie z właściwym diagramem płyty.
4. Uruchom **MODI-Setup.exe**.
5. Wybierz lub pozwól wykryć zgodną instalację **J-Runner with Extras 3.4.0.7**.
6. Kliknij **Zainstaluj MODI TURBO**. Oryginalny J-Runner pozostaje bez zmian.
7. Podłącz MODI Pico 2 Flasher X360 TURBO.
8. Przed zapisem wykonaj **READ → BACKUP → COMPARE/VERIFY**.

Szczegółowa instrukcja: [Instalacja PL](docs/INSTALL_PL.md) · [English](docs/INSTALL.md)

## Dlaczego MODI?

Na początku sceny Xbox 360 operacje NAND na starszych interfejsach, takich jak LPT, mogły trwać dziesiątki minut. Programatory USB mocno to przyspieszyły. Dzisiejsze tanie mikrokontrolery pozwalają zrobić kolejny krok.

MODI powstał z prostym założeniem: **szybki serwis pamięci Xbox 360 ma być dostępny na tanim sprzęcie i nie wymagać od użytkownika środowiska deweloperskiego.**

Projekt skupia się na:

- serwisie NAND Xbox 360
- Corona eMMC
- Jasper Big Block
- pracy serwisowej przy RGH
- backupie i odzyskiwaniu NAND
- integracji z J-Runner
- Right to Repair

## Tani sprzęt

Projekt celuje w niedrogie płytki RP2350 / Pico 2. Samą płytkę bazową można często kupić za około **5–6 USD**, zależnie od regionu i dostawcy. Kwota dotyczy samej płytki, bez przewodów, adapterów i wysyłki.

## THE NEXT STEP: MODI X360 ULTIMATE

**All-in-One Xbox 360 Service Tool · ULTIMATE PREVIEW / IN DEVELOPMENT**

![MODI X360 ULTIMATE](assets/logo/modi-x360-ultimate-transparent.png)

TURBO pozostaje sprawdzonym modułem flashowania. ULTIMATE rozwija go w docelową platformę serwisową: backup, RGH, CPU Key, Audio/Sonus, programowanie chipów, LIVE i konwersje pamięci.

**ONE DEVICE. ONE HEADER. ONE SOFTWARE. FULL XBOX 360 SERVICE WORKFLOW.**

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

[ULTIMATE](docs/ULTIMATE_PL.md) · [Conversions](docs/CONVERSIONS_PL.md) · [Alpha](docs/ALPHA_PL.md) · [Wiring](docs/FLASHSHIP_WIRING_PL.md)

**MODI Audio RDY = GP22; GP11 = passive SMB_DATA.**

Stable: sprawdzona baza TURBO. Alpha: nowe moduły wymagające walidacji sprzętowej.


## Podziękowania

Projekt opiera się na wielu latach pracy społeczności Xbox 360.

Szczególne podziękowania dla **Team Jungle**, **Team Xecuter**, **Octal450**, **J-Runner-With-Extras contributors**, **Mitchell Waite / mitchellwaite**, **Pheeeeenom / Mena**, **Balázs Triszka / balika011**, **X360Tools contributors** oraz wszystkich osób dokumentujących NAND, eMMC, RGH/JTAG i naprawy płyt Xbox 360.

Integracja MODI / kierunek projektu: **Kacper Lewandowski · modyfikatorcasper · Modyfikator89 · Modi · MODI Diagnostic Lab**.

Pełne credits: [CREDITS.md](CREDITS.md)

## Source firmware i licencje

Dystrybuowany UF2 MODI zawiera firmware wywodzący się z prac PicoFlasher. Odpowiadające źródło firmware oraz wymagane informacje third-party pozostają dostępne przy wydaniu w celu zachowania zgodności licencyjnej.

[Pobierz paczkę source / compliance](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-stable/MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip)

Zobacz też: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)

## Niezależny projekt

**Niezależny projekt fanowski i społecznościowy.** MODI Pico 2 Flasher X360 TURBO i MODI Diagnostic Lab nie są powiązane, sponsorowane, wspierane ani zatwierdzone przez Microsoft lub Xbox. Nazwy i znaki Xbox należą do ich właścicieli i są używane wyłącznie do identyfikacji kompatybilnego sprzętu oraz dokumentacji technicznej i serwisowej.

[Pełny disclaimer](DISCLAIMER.md) · [Status wydania i hashe](docs/RELEASE_STATUS_PL.md)

**Strona projektu:** https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/

