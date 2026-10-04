# Instalacja — MODI Pico 2 Flasher X360 TURBO

[English](INSTALL.md)

## Wymagania

Windows z .NET Framework 4.8, pełna oficjalna instalacja J-Runner with Extras 3.4.0.7 oraz Pico 2 / zgodna płytka RP2350. Foldery `common` i `xeBuild` muszą zostać obok oryginalnego `JRunner.exe`.

Wgraj [UF2 na Pico 2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2), potem pobierz [pełną paczkę MODI ZIP](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip) oraz [oficjalną bazę J-Runner 3.4.0 r7](https://github.com/J-Runner-With-Extras/J-Runner-with-Extras/releases/tag/V3.4.0-r7).

## Instalacja

1. Pobierz i rozpakuj `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip`.
2. Podłącz Pico 2 z przytrzymanym BOOTSEL i skopiuj dołączony UF2 na wykryty dysk. Poczekaj na restart.
3. Uruchom `MODI-Setup.exe`. Wybierz wykrytą zgodną instalację albo kliknij **Wybierz JRunner.exe** i wskaż oryginał.
4. Kliknij **Zainstaluj MODI TURBO**. Instalator działa offline, sprawdza dokładny SHA256 oryginału i tworzy gotowy `JRunner.MODI.exe` obok niego.
5. Kliknij **Uruchom MODI** albo uruchom ten plik bezpośrednio.
6. Podłącz przewody i zasilanie zgodnie z procedurą serwisową danej płyty. Sprawdź urządzenie i typ pamięci; wykonaj dwa READ i porównaj je przed WRITE.

Oryginalny `JRunner.exe`, pliki pomocnicze i biblioteki zewnętrzne pozostają na miejscu. Instalator nie wymaga uprawnień administratora, jeśli folder instalacji pozwala na zapis.

## Pinout / Header — MODI Pico 2 Flasher X360 TURBO

Piny naszego headera NAND/SPI na Waveshare RP2350-Plus:

| Pozycja headera¹ | Kolor przewodu | Pin RP2350 | Sygnał | Punkt Corona / Trinity | Punkt Falcon / Fat |
|---:|---|---|---|---|---|
| 1 | Pomarańczowy | GP0 | SPI_MISO | J2C1.4 | J1D2.4 |
| 2 | Brązowy | GP1 | SPI_SS_N | J2C1.2 | J1D2.2 |
| 3 | Żółty | GND | GND | J2C1.6 | J1D2.6 |
| 4 | Czerwony | GP2 | SPI_CLK | J2C1.3 | J1D2.3 |
| 5 | Czarny | GP3 | SPI_MOSI | J2C1.1 | J1D2.1 |
| 6 | Niebieski | GP4 | SMC_DBG_EN | J2C3.6 | J2B1.6 |
| 7 | Zielony | GP5 | SMC_RST_XDK_N | J2C3.5 | J2B1.5 |

¹ Licz od strony USB w dół **siedmiopozycyjnego headera MODI ze zdjęcia**. Przy USB u góry header znajduje się **po lewej od przodu** (elementy / BOOT / RESET), a **po prawej od tyłu** (napisy GPIO).

Kolejność fizyczna: **GP0 → GP1 → GND → GP2 → GP3 → GP4 → GP5**.

**Żółty to GND. Czarny to SPI_MOSI.** Numery GPIO nie są numerami pozycji headera. Masa jest między GP1 i GP2. `J2C1.4` oznacza punkt 4 złącza J2C1, nie GPIO 4. Ustal punkt 1 z oznaczeń płyty / kwadratowego pola i zachowaj orientację ze zdjęcia; nie licz punktów według kolejności przewodów.

Diagramy oraz procedura połączenia: [Corona, Trinity i Falcon / Fat](WIRING_PL.md).

## Zgodność i ponowna instalacja

Wymagany SHA256 oryginału: `44F647B213B80489DBA0E396DDA262609BDF59D6F271DB416CDFE02507F8B39F`.

Ponowny start sprawdza identyczną instalację MODI. Niezgodny oryginał, brak folderów pomocniczych lub inny istniejący `JRunner.MODI.exe` powodują przerwanie bez podmiany pliku. Aby zainstalować nową wersję obok starszej, rozpakuj świeżą oficjalną kopię J-Runnera do innego folderu i wskaż jej oryginalny plik.

Zachowaj `MODI-install-receipt.txt`. Aby wrócić do wersji stock, uruchom niezmieniony oryginał. Zamknij obie wersje przed przełączeniem.

## Kontrola

Sprawdź SHA256 paczki. Zachowaj zweryfikowany backup. Porównanie plików nie potwierdza fizycznego odczytu po zapisie. Po WRITE wykonaj READ BACK, porównaj wybrany zakres i potwierdź start konsoli.

## Zgłoszenie problemu

Podaj treść błędu, Windows, wersję Setup, J-Runnera, firmware, płytę i pamięć. Nie dołączaj CPU key ani prywatnych dumpów. To publiczna 0.9.1 Beta; użytkownik potwierdził testy sprzętowe 2026-10-04.
