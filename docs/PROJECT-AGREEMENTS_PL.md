# FLASHSHIP / ULTIMATE — główne ustalenia projektu

Ustalone przez właściciela projektu: **8 października 2026**. Hasło „wracamy do FLASHSHIP / ULTIMATE” oznacza ten zestaw założeń.

[English](PROJECT-AGREEMENTS.md) · [DEVLOG / LAB NOTES](DEVLOG_PL.md) · [Obecny stan ULTIMATE](ULTIMATE_PL.md)

## Nazwy i filozofia

| Nazwa | Znaczenie |
|---|---|
| **MODI FLASHSHIP** | Fizyczna płytka / urządzenie na RP2350. Nazwa łączy FLASH + FLAGSHIP. |
| **MODI X360 ULTIMATE** | Cały docelowy system i oprogramowanie serwisowe. |
| **TURBO** | Moduł szybkiego NAND/eMMC, nie nazwa całego ekosystemu. |
| **MODI Chip Flasher** | Funkcja programowania glitch chipów; wykorzystanie DirtyJTAG opisujemy w credits i licencjach. |

**ONE DEVICE. ONE HEADER. ONE SOFTWARE.**

Zasada od Lewego: nie wymyślamy koła na nowo. Korzystamy ze sprawdzonych elementów sceny i zachowujemy autorstwo. Przewagę budujemy integracją, automatyzacją, szybkością i prostotą.

To docelowa architektura. Obecny Alpha nadal używa osobnych profili UF2; jedno wspólne firmware i automatyczne przełączanie trybów wymagają realizacji i testów.

## Automatic RGH — cel

2× dump → compare → przygotowanie XeLL → flash → start konsoli → automatyczne przechwycenie CPU Key → sprawdzenie klucza → automatyczny build image → flash finalnego NAND → readback / verify.

Dwa zgodne backupy, prawidłowe rozpoznanie pamięci i walidacja danych konsoli są bramkami przed zapisem. Niepewne dane zatrzymują operację.

Przy założeniu około 18 s + 18 s + 24 s sama ścieżka pamięci do XeLL-a zajmuje około **60 s**. To suma orientacyjnych czasów, nie zmierzony pełny Automatic RGH. Publiczna tabela TURBO nadal podaje około 19 s READ i 24 s WRITE dla testowanego NAND 16 MB.

Cel serwisowy: kilka–kilkanaście minut całej pracy dla sprawnego serwisanta, razem z rozebraniem i lutowaniem. Część programowa ma być praktycznie bezobsługowa. Nie jest to obecna gwarancja ani wynik pomiaru.

## Moduły

TURBO NAND/eMMC, Audio/Sonus, MODI Chip Flasher, UART/COM, HANA/SMBus LIVE, później konwersje pamięci i kolejne funkcje.

CPU Key: automatyczne przechwycenie z obsługiwanej ścieżki XeLL; LAN jest obecną alternatywą. Nasłuch SMBus/HANA sam w sobie nie dostarcza CPU Key ani pełnego testu HDMI.

## Konwersje — obrazy pod fizyczną wymianę pamięci

- Corona 4 GB → NAND 16 MB: osobne ścieżki V2 i V4.
- Winchester → NAND 16 MB: z odpowiednimi danymi konsoli pozyskanymi przez obsługiwaną metodę, np. Bad Update; nie klasyczne RGH.
- Jasper Big Block 256 MB → NAND 16 MB.
- Jasper Big Block 512 MB → NAND 16 MB.

Maksymalna automatyzacja, z kontrolą danych wejściowych, odczytem kontrolnym i testem startu dla każdej kombinacji. Konwersje są w rozwoju. DVD Remarry pozostaje dalszym projektem badawczym.

## Programowanie chipów i zasilanie

Dążymy do pracy bez dodatkowego programatora. Luźny chip może otrzymywać 3,3 V z FLASHSHIP po potwierdzeniu zgodności jego napięcia i obciążenia z płytką. Jeśli chip jest już zasilany przez konsolę, nie dokładamy drugiego zasilania. Mapa konkretnego modelu chipu pozostaje źródłem połączeń.

## Dokumentacja i własne fotografie

Na grafikach urządzenie podpisujemy **MODI FLASHSHIP**, z dopiskiem modelu RP2350-Plus, gdy potrzebne jest rozróżnienie sprzętu.

Przygotowujemy własne zdjęcia: przód i tył RP2350-Plus, potem makra wszystkich punktów konsol i chipów. Obce fotografie są tymczasowymi referencjami; finalna dokumentacja ma używać własnych zdjęć. Do czasu ich zastąpienia zachowujemy źródła i autorów. Nie oznaczamy cudzej fotografii jako własnej.

## DEVLOG / LAB NOTES

Dziennik na GitHub Pages zapisuje pomysły, rozwój, testy, porażki i rozwiązania.

| Status | Znaczenie |
|---|---|
| IDEA | Pomysł bez potwierdzonej realizacji. |
| RESEARCH | Badanie dokumentacji i wykonalności. |
| PROTOTYPE | Istniejący prototyp; walidacja niepełna. |
| TESTED | Test wykonany w opisanym zakresie i konfiguracji. |
| VERIFIED | Wynik potwierdzony z zapisaną metodą i dowodami, np. compare/readback. |

Każdy wpis: data, moduł, status, wersja, konfiguracja, obserwacja, wynik i następny krok. VERIFIED dotyczy wskazanego testu, nie automatycznie całego produktu.

Pierwszy większy wpis: od prostego flashera za kilka dolarów do **FLASHSHIP + X360 ULTIMATE**.

## Publikacja

Użytkownik dostaje gotowe pliki i prostą instalację. Prywatny kod aplikacji MODI pozostaje prywatny. Wymagane źródła odpowiadające rozpowszechnianemu firmware i notices pozostają dostępne zgodnie z licencjami. Ustalenia nie zmieniają bajtów przetestowanych UF2/Setup ani wyników testów.
