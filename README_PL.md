# MODI Pico 2 Flasher X360 TURBO

**🇵🇱 Polski** · [🇬🇧 English](README.md)

> **Szybki programator serwisowy NAND i eMMC dla Xbox 360**  
> tani sprzęt RP2350 · integracja z J-Runner with Extras · projekt społecznościowy nastawiony na naprawę

> **STATUS WYDANIA:** [0.9.1 Beta jest publiczna](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta). Instalacja offline i testy integracji przeszły. Użytkownik potwierdził poprawne testy sprzętowe 2026-10-04. Prawdziwy screenshot aplikacji nadal czeka.

## Pobierz

**[Pobierz gotową paczkę ZIP](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip)** · [UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2) · [SHA256](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/SHA256SUMS.txt) · [Źródła firmware](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-corresponding-source-v0.9.1.zip)

![MODI Pico 2 Flasher X360 TURBO](assets/logo/modi-turbo.png)

![HIGH SPEED → TURBO](assets/gif/high-speed-to-turbo.gif)


---

## Co to jest?

MODI Pico 2 Flasher X360 TURBO to niezależny projekt społecznościowy zbudowany wokół taniej płytki **RP2350 / Pico 2**, przeznaczony do szybkiej pracy serwisowej z pamięciami NAND i eMMC w Xbox 360.

Kiedy rozwijała się scena RGH, odczyt i zapis NAND-u na starszych interfejsach, takich jak LPT, potrafił trwać dziesiątki minut. Programatory USB zmieniły ten obraz. Dzisiaj niedrogie i bardzo wydajne mikrokontrolery pozwalają pójść jeszcze dalej.

Projekt powstał z prostego pytania: **jak daleko można przyspieszyć tanią płytkę RP2350, zachowując pewny, zweryfikowany bajt po bajcie zapis?**

Kiedy zaczynałem jako serwisant, sam korzystałem z wiedzy i narzędzi tworzonych przez społeczność Xbox 360. Po latach napraw, diagnostyki i pracy ze sprzętem chcę oddać tej społeczności coś od siebie: praktyczne narzędzie, dokumentację i wiedzę, które pomagają naprawiać sprzęt zamiast go wyrzucać.

## Potwierdzone wyniki sprzętowe

| Pamięć / testowany zakres | READ | WRITE |
|---|---:|---:|
| NAND 16 MB | ~19 s | ~24 s |
| Jasper Big Block — testowany zakres 64 MiB + spare | 76.890–76.955 s | 90.171 s |
| Corona eMMC — testowany zakres 48 MiB | 56.198–57.792 s | 48.310 s |

**Wyniki uzyskano na testowanym sprzęcie. Rzeczywiste czasy mogą się różnić zależnie od płyty, jakości połączeń, hosta USB i konfiguracji systemu.** Są to wyniki sprzętowe MODI Flasher, a nie benchmark instalatora.

Na obecnym etapie opisujemy MODI jako **jedno z najszybszych tanich rozwiązań do flashowania Xbox 360, jakie przetestowaliśmy**. Zanim użyjemy bezwzględnego hasła „najszybszy na świecie”, potrzebne jest publiczne porównanie z aktualnie dostępnymi rozwiązaniami.

## Główny cel: naprawa

To narzędzie powstało przede wszystkim do **serwisu, backupu, odzyskiwania i naprawy sprzętu**. Uszkodzony lub skorumpowany NAND/eMMC może uniemożliwić naprawę konsoli bez odpowiedniego sprzętu.

**Right to Repair / Prawo do naprawy:** wspieramy zasadę, że właściciele sprzętu i niezależne serwisy powinni mieć praktyczny dostęp do narzędzi i wiedzy technicznej potrzebnej do diagnozowania, konserwacji i naprawy własnego sprzętu.

Projekt nie jest oficjalnym narzędziem Microsoft/Xbox. Użytkownik odpowiada za sposób użycia narzędzia i zgodność z obowiązującym prawem.

## Tani sprzęt

Projekt celuje w niedrogie płytki Pico 2 / RP2350. Samą płytkę bazową można często kupić za około **5–6 USD**, zależnie od dostawcy i regionu. Kwota dotyczy **samej płytki deweloperskiej** — bez przewodów, adapterów, wysyłki i dodatkowych akcesoriów.

## Szybki start

1. Pobierz i rozpakuj **MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip** z odpowiedniego GitHub Release.
2. Uruchom Pico 2 / zgodną płytkę RP2350 w trybie **BOOTSEL** i skopiuj plik UF2 na wykryty dysk.
3. Podłącz programator do właściwych punktów NAND/eMMC na płycie Xbox 360.
4. Uruchom **MODI-Setup.exe** z rozpakowanej paczki.
5. Wybierz wykrytą instalację **J-Runner with Extras 3.4.0.7** albo wskaż ją przyciskiem **Wybierz JRunner.exe**.
6. Kliknij **Zainstaluj MODI TURBO**. Instalator modyfikuje zweryfikowaną kopię offline i tworzy gotowy `JRunner.MODI.exe`; oryginał pozostaje bez zmian.
7. Podłącz MODI Pico 2 Flasher X360 TURBO.
8. **READ → BACKUP → COMPARE/VERIFY przed każdym WRITE.**

Szczegółowa instrukcja: [Instalacja PL](docs/INSTALL_PL.md) · [English](docs/INSTALL.md)

## Co publikujemy

W publicznym wydaniu mają znaleźć się wyłącznie rzeczy potrzebne użytkownikowi:

- jeden ZIP z `MODI-Setup.exe`, UF2 oraz START-HERE PL/EN
- `MODI-Pico2-Flasher-X360-TURBO.uf2`
- `SHA256SUMS.txt`
- instrukcje / release notes
- odpowiadające źródło firmware lub czytelny link do niego zgodny z GPL

**Nie publikujemy pełnego zmodyfikowanego drzewa J-Runnera, workspace deweloperskiego, prywatnych dumpów, CPU key, cache ani zewnętrznych DLL o niejasnych prawach redystrybucji.**

## MODI FLASHSHIP — Co dalej

| Funkcja | Status |
|---|---|
| Audio / Sonus | 🔜 **COMING SOON** — trwają testy sprzętowe |
| DirtyJTAG / programowanie glitch chipów | 💡 **PLANNED** |
| UART / COM monitor | 💡 **PLANNED** |
| Diagnostyka HANA | 🔬 **RESEARCH** |
| Natywne wsparcie w upstream J-Runner | 🧩 **PROPOSED** |

Szczegóły: [MODI FLASHSHIP PL](docs/FLASHSHIP_PL.md) · [English](docs/FLASHSHIP.md)

## Podziękowania

Projekt istnieje dzięki wielu latom pracy społeczności Xbox 360.

Szczególne podziękowania dla:

- **Team Jungle** i **Team Xecuter** — za historię i fundamenty narzędzi związanych z J-Runnerem i serwisem Xbox 360.
- **Octal450** — za J-Runner with Extras i lata dalszego rozwoju projektu.
- **J-Runner-With-Extras organization oraz wszystkim contributorom**, w tym osobom rozwijającym najnowsze wydania, takim jak **Mitchell Waite / mitchellwaite**.
- **Pheeeeenom / Mena** — za wkład w obecny ekosystem wydań/dystrybucji J-Runner with Extras.
- **Balázs Triszka / balika011** — za oryginalny PicoFlasher.
- **X360Tools contributors** — za dalszy rozwój PicoFlashera.
- Wszystkim, którzy przez lata dokumentowali naprawy Xbox 360, NAND, eMMC, RGH/JTAG i diagnostykę płyt.

Integracja MODI / projekt: **MODI Diagnostic Lab · Modyfikator89**.

Pełne credits: [CREDITS.md](CREDITS.md)

## Licencje

Oryginalne teksty licencji third-party pozostają nietknięte. Polskie tłumaczenia, jeśli powstaną, są wyłącznie tłumaczeniami informacyjnymi.

Firmware MODI jest pochodną projektu PicoFlasher objętego GPL. Jeżeli dystrybuujemy zmodyfikowany UF2, odpowiadające mu źródło musi być dostępne zgodnie z GPL. Główne repo wydania pozostaje czyste; źródło firmware może być umieszczone w osobnym repo lub jako odpowiadające archiwum źródłowe, ale musi być jasno podlinkowane.

Zobacz: [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)

## Niezależny projekt / disclaimer

**Niezależny projekt fanowski i społecznościowy.** MODI Pico 2 Flasher X360 TURBO i MODI Diagnostic Lab nie są powiązane, sponsorowane, wspierane ani zatwierdzone przez Microsoft lub Xbox. Nazwy i znaki Xbox należą do ich właścicieli i są używane wyłącznie do identyfikacji kompatybilnego sprzętu oraz dokumentacji technicznej i serwisowej.

Pełny disclaimer: [DISCLAIMER.md](DISCLAIMER.md)


## Stan paczki i źródła firmware

[Status wydania i hashe](docs/RELEASE_STATUS_PL.md) · [Odpowiadające źródła firmware](docs/FIRMWARE_SOURCE.md)

