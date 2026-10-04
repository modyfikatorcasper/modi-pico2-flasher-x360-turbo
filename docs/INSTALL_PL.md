# Instalacja — MODI Pico 2 Flasher X360 TURBO

[English](INSTALL.md)

## Wymagania

- Windows x64
- .NET Framework 4.8
- zgodna instalacja J-Runner with Extras 3.4.0.7
- Raspberry Pi Pico 2 / zgodna płytka RP2350
- odpowiedni plik `MODI-Pico2-Flasher-X360-TURBO.uf2`
- przewody i poprawne punkty serwisowe dla danej płyty Xbox 360
- połączenie z Internetem podczas pierwszego uruchomienia MODI Setup

## 1. Flashowanie Pico 2

1. Odłącz Pico 2 od USB.
2. Przytrzymaj przycisk **BOOTSEL**.
3. Podłącz USB, nadal trzymając BOOTSEL.
4. Zwolnij przycisk po pojawieniu się dysku USB.
5. Skopiuj plik `MODI-Pico2-Flasher-X360-TURBO.uf2` na wykryty dysk.
6. Płytka automatycznie uruchomi się ponownie z firmware MODI.

Zawsze używaj UF2 z tego samego wydania co dokumentacja i sprawdź SHA256 przed użyciem.

## 2. Przygotowanie J-Runnera

MODI Setup **nie nadpisuje** oryginalnego `JRunner.exe`.

1. Pobierz `MODI-Setup.exe` z GitHub Releases.
2. Uruchom instalator.
3. Wskaż istniejący, zgodny `JRunner.exe` w wersji 3.4.0.7.
4. Instalator zweryfikuje wymagane pliki i wersje.
5. Przy pierwszym uruchomieniu pobierze wymagane, przypięte komponenty builda.
6. Prywatne .NET SDK jest używane lokalnie — instalator nie zmienia globalnego PATH.
7. Po zakończeniu obok oryginału powstanie `JRunner.MODI.exe`.

Oryginalny `JRunner.exe` pozostaje bez zmian.

## 3. Pierwsze uruchomienie

1. Uruchom `JRunner.MODI.exe`.
2. Podłącz MODI Pico 2 Flasher X360 TURBO.
3. Sprawdź, czy program rozpoznaje urządzenie jako MODI.
4. Potwierdź wykryty typ pamięci przed operacją.

## 4. Najważniejsza zasada

**Zawsze najpierw wykonaj READ i backup.**

Zalecany workflow:

1. READ / backup 1
2. READ / backup 2, jeśli workflow tego wymaga
3. COMPARE / VERIFY plików
4. dopiero wtedy WRITE
5. po zapisie wykonaj odczyt kontrolny / porównanie, jeżeli wymaga tego dana procedura serwisowa

`VERIFY` dotyczący porównania plików nie zawsze oznacza automatyczny fizyczny odczyt kontrolny po WRITE.

## 5. Cache i logi

MODI Setup używa katalogów w `%LOCALAPPDATA%\MODI\Setup\`.

Przykładowo:

- cache: `%LOCALAPPDATA%\MODI\Setup\downloads`
- log przebiegu: `%LOCALAPPDATA%\MODI\Setup\run-ID\setup.log`

## 6. Usunięcie MODI

Ponieważ oryginalny J-Runner nie jest nadpisywany, powrót do wersji stock jest prosty:

- zamknij J-Runner,
- usuń `JRunner.MODI.exe`, jeśli nie chcesz go dalej używać,
- opcjonalnie usuń cache / receipt MODI Setup,
- uruchom ponownie oryginalny `JRunner.exe`.

## 7. Bezpieczeństwo

- nie zapisuj przypadkowego obrazu NAND/eMMC,
- nie udostępniaj publicznie CPU key ani prywatnych dumpów,
- sprawdzaj SHA256 pobranych plików,
- przed WRITE zawsze upewnij się, że masz poprawny i zweryfikowany backup,
- błędne podłączenie lub zasilanie może uszkodzić sprzęt.

## 8. Gdy instalator zgłasza błąd

Zachowaj `setup.log` i przy zgłoszeniu podaj:

- wersję Windows,
- wersję MODI Setup,
- wersję J-Runner,
- wersję firmware MODI,
- płytę Xbox 360,
- typ pamięci,
- etap, na którym wystąpił błąd.

Nie dołączaj prywatnych dumpów ani CPU key.
