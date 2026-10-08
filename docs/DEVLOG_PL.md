# DEVLOG / LAB NOTES

[English](DEVLOG.md) · [Ustalenia projektu](PROJECT-AGREEMENTS_PL.md) · [Dziennik na stronie](https://modyfikatorcasper.github.io/modi-pico2-flasher-x360-turbo/#devlog)

Statusy: **IDEA / RESEARCH / PROTOTYPE / TESTED / VERIFIED**. Zakres i dowody są obowiązkowe przy statusie VERIFIED.

## 2026-10-08 — od prostego flashera do FLASHSHIP + X360 ULTIMATE

**Moduł:** architektura / historia projektu  
**Status:** RESEARCH — docelowy system; TESTED — wskazane transfery TURBO; PROTOTYPE — dodatkowe profile Alpha  
**Wersje:** TURBO v0.9.1-stable, dodatkowe profile v1.0.0-alpha.1  
**Konfiguracja:** RP2350 / Pico 2, integracja J-Runner; wyniki odnoszą się do poszczególnych przetestowanych płyt i zakresów.

### Punkt wyjścia

Zaczęliśmy od prostego, niedrogiego flashera opartego na pracy sceny PicoFlasher i J-Runner. Pierwszy cel był konkretny: zrzut i zapis NAND/eMMC, widoczny postęp, osobny czas READ i WRITE oraz porównanie danych. Sprawdzone elementy społeczności były bazą; MODI rozwija integrację i obsługę.

### TURBO i próby, które nie przeszły

Optymalizacje firmware i hosta obejmowały transfery PIO/DMA, potokowanie oraz potwierdzanie zapisanych stron/sektorów. Nie każdy szybszy wariant był stabilny. W historii testów pojawiały się przerwane odczyty eMMC, błędne Flash Config, zatrzymane zapisy i porównanie NAND kończące się wyjątkiem. Jeden problem eMMC wynikał z uszkodzonej konsoli, a nie z samego flashera. Przerwane transfery nie są poprawnymi benchmarkami.

Wniosek: krótszy czas nie wystarcza. Potrzebujemy pełnej operacji, zgodnych dumpów, readback po zapisie i startu konsoli w określonym teście. Działająca baza pozostaje zachowana, a eksperymenty są od niej oddzielone.

### Wyniki zapisane w publicznej tabeli

| Pamięć / zakres | READ | WRITE | Zakres wniosku |
|---|---:|---:|---|
| NAND 16 MB | ~19 s | ~24 s | Orientacyjne czasy testowanego zakresu. |
| Jasper Big Block, 64 MiB + spare | 76.890–76.955 s | 90.171 s | Dwa odczyty były zgodne bajt po bajcie; sam komunikat Write Successful nie zastępuje readback. |
| Corona eMMC, 48 MiB | 56.198–57.792 s | 48.310 s | Wyniki z tabeli TURBO; nie są pomiarem całego RGH. |

Nie zmieniamy starych wyników na podstawie nowych założeń. W tym wpisie nie wykonano nowych testów sprzętowych.

### Rozdzielenie nazw

**FLASHSHIP** to nasze urządzenie na RP2350 — FLASH + FLAGSHIP. **X360 ULTIMATE** to docelowy cały system. **TURBO** jest jego szybkim modułem NAND/eMMC.

**ONE DEVICE. ONE HEADER. ONE SOFTWARE.**

Obecny Alpha uruchamia osobne profile UF2. Dodatkowe GPIO umożliwiają rozwój Audio/Sonus, MODI Chip Flasher, UART/COM i HANA/SMBus LIVE. Wspólne firmware i program nie są jeszcze gotowym, zweryfikowanym produktem.

### Następne etapy

Automatic RGH: 2× dump → compare → XeLL → flash → start → CPU Key → build image → flash → verify. Około 18 + 18 + 24 = 60 s dotyczy wyłącznie orientacyjnej ścieżki pamięci do XeLL-a. Cała automatyzacja i czas pracy serwisowej pozostają celami.

Konwersje obejmują osobne Corona V2/V4 4 GB, Winchester z wymaganymi danymi konsoli oraz Jasper BB 256/512 MB — obrazy pod fizyczną wymianę na NAND 16 MB. DVD Remarry pozostaje RESEARCH.

### Dokumentacja

Własne zdjęcia przodu/tyłu FLASHSHIP i makra punktów zastąpią tymczasowe fotografie referencyjne. Do tego czasu źródła i autorzy pozostają widoczni. Na docelowych grafikach płytkę podpisujemy MODI FLASHSHIP.

### Własny wkład

Własny projekt powinien wnosić rzeczywisty wkład: nowe możliwości, lepszą dostępność albo usprawnienia, których wcześniej brakowało. Research i reverse engineering wymagają czasu, często tygodni lub lat, zanim mały krok otworzy drogę do następnego. W MODI rozwijamy spójne narzędzie serwisowe i własne rozwiązania, a cudzą pracę opisujemy z zachowaniem autorstwa.

### Następny krok / warunek VERIFIED

Wspólne tryby wymagają testów sprzętowych: Audio backup/write/readback/play, chip IDCODE/program/verify, UART i równoczesny SMBus. Automatic RGH i każda konwersja potrzebują własnego pełnego scenariusza, readback i potwierdzenia startu. Do wpisu dołączamy wersję, konfigurację oraz odnośnik do wyników bez dumpów, kluczy i danych klientów.

## Szablon kolejnego wpisu

- Data / moduł / status:
- Wersja firmware i hosta:
- Konfiguracja sprzętu i zakres:
- Hipoteza:
- Próba / obserwacja:
- Wynik i dowód:
- Porażka / rozwiązanie:
- Następny krok:

## Zasada od Lewego

Nie wymyślaj koła na nowo.
