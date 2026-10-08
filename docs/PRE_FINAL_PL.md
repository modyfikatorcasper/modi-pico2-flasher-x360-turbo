# MODI pre-final i ostatni etap wydania

[English](PRE_FINAL.md) · [Podłączenia Audio i DirtyJTAG](FLASHSHIP_WIRING_PL.md)

Lokalna paczka pre-final z 8 października 2026 zbiera sprawdzoną bazę TURBO oraz istniejące preview Audio, DirtyJTAG i LIVE. Publicznym wydaniem pozostaje [v0.9.1-beta](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/tag/v0.9.1-beta). Diagramy i instrukcje preview są publiczne; pełny lokalny JRunner.exe preview wymaga zakończenia audytu dystrybucji.

## Zakres paczki

| Element | Stan |
|---|---|
| TURBO NAND/eMMC i MODI-Setup.exe | Sprawdzone binaria, zachowane bajty i hashe |
| Audio Sonus | Kompilacja i testy offline zaliczone; testy sprzętowe do wykonania |
| DirtyJTAG ACE V3 / CoolRunner / Matrix | SVF/XSVF preview; testy chipów do wykonania |
| ACE V3+ / V4 / V5 Gowin | Backend .fs niezaimplementowany |
| UART oraz pasywny SMBus/HANA | Równoczesny nasłuch zaimplementowany w LIVE; walidacja sprzętowa do wykonania |
| XeLL po LAN | Panel lokalnego preview; kontrola klucza i zapis lokalny |
| Obraz pod wymianę pamięci na NAND 16 MB | Ostatnia planowana funkcja; niezaimplementowana |

Setup nadal instaluje dotychczasową bazę. Nowy EXE LIVE jest osobnym dodatkiem do kopii kompletnej instalacji. Audio/DirtyJTAG mają własny panel MODI-Flashship. Jeden Pico uruchamia jeden profil UF2; nie ma jeszcze firmware łączącego wszystkie programatory i nasłuchy.

## Ostatnia funkcja przed finałem

Potwierdzony cel: jedno kliknięcie przygotowuje obraz pod **fizyczną wymianę** Corona eMMC lub Jasper NAND 256/512 MB na kompatybilny NAND 16 MB. Obsługa konkretnej rewizji i układu docelowego musi zostać potwierdzona przed udostępnieniem funkcji.

Planowany przebieg:

1. Zachowanie oryginalnych kopii oraz sprawdzenie zgodności niezależnych odczytów i hashy.
2. Rozpoznanie płyty, geometrii źródła, ECC/spare, remapów i danych tej konsoli; weryfikacja CPU Key, gdy potrzebna.
3. Sprawdzenie zgodności fizycznego układu 16 MB, połączeń, konfiguracji płyty, bootloaderów i SMC.
4. Wygenerowanie obrazu z danymi tej konsoli, geometrią i ECC/remapami dla celu 16 MB.
5. Niezależna walidacja, zapis nowego pliku i raport z hashami. Brak zgodności zatrzymuje operację.

To wymaga przebudowy zgodnego obrazu; samo obcięcie dumpu nie wystarcza. Oprogramowanie nie zmienia fizycznego interfejsu pamięci ani konfiguracji sprzętowej. Przygotowanie obrazu nie uruchamia automatycznie zapisu do konsoli. Zapis docelowego układu i pełny odczyt kontrolny są osobnym etapem po weryfikacji sprzętu.

## Warunki finalnego wydania

Konwersja musi przejść testy obrazów oraz pełny zapis, zgodny odczyt i start rzeczywistych konsol dla obsługiwanych rewizji. Nowe moduły wymagają testów Audio, chipów JTAG i jednoczesnego UART/SMBus. Pełny host wymaga dopięcia audytu dystrybucji lub wydania w formie patch/updater.

Publiczne wydanie zachowa cztery assety: główny UF2, kompletna paczka instalacyjna, jeden SOURCE ZIP ze źródłami wszystkich rozpowszechnianych profili firmware oraz SHA256SUMS.txt. Prywatne źródła MODI-Setup, J-Runnera i integracji MODI pozostają poza publicznym repo.
