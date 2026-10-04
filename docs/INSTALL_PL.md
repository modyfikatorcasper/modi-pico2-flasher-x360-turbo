# Instalacja — MODI Pico 2 Flasher X360 TURBO

[English](INSTALL.md)

## Wymagania

Windows z .NET Framework 4.8, pełna oficjalna instalacja J-Runner with Extras 3.4.0.7 oraz Pico 2 / zgodna płytka RP2350. Foldery `common` i `xeBuild` muszą zostać obok oryginalnego `JRunner.exe`.

## Instalacja

1. Pobierz i rozpakuj `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip`.
2. Podłącz Pico 2 z przytrzymanym BOOTSEL i skopiuj dołączony UF2 na wykryty dysk. Poczekaj na restart.
3. Uruchom `MODI-Setup.exe`. Wybierz wykrytą zgodną instalację albo kliknij **Wybierz JRunner.exe** i wskaż oryginał.
4. Kliknij **Zainstaluj MODI TURBO**. Instalator działa offline, sprawdza dokładny SHA256 oryginału i tworzy gotowy `JRunner.MODI.exe` obok niego.
5. Kliknij **Uruchom MODI** albo uruchom ten plik bezpośrednio.
6. Podłącz przewody i zasilanie zgodnie z procedurą serwisową danej płyty. Sprawdź urządzenie i typ pamięci; wykonaj dwa READ i porównaj je przed WRITE.

Oryginalny `JRunner.exe`, pliki pomocnicze i biblioteki zewnętrzne pozostają na miejscu. Instalator nie wymaga uprawnień administratora, jeśli folder instalacji pozwala na zapis.

## Zgodność i ponowna instalacja

Wymagany SHA256 oryginału: `44F647B213B80489DBA0E396DDA262609BDF59D6F271DB416CDFE02507F8B39F`.

Ponowny start sprawdza identyczną instalację MODI. Niezgodny oryginał, brak folderów pomocniczych lub inny istniejący `JRunner.MODI.exe` powodują przerwanie bez podmiany pliku. Aby zainstalować nową wersję obok starszej, rozpakuj świeżą oficjalną kopię J-Runnera do innego folderu i wskaż jej oryginalny plik.

Zachowaj `MODI-install-receipt.txt`. Aby wrócić do wersji stock, uruchom niezmieniony oryginał. Zamknij obie wersje przed przełączeniem.

## Kontrola

Sprawdź SHA256 paczki. Zachowaj zweryfikowany backup. Porównanie plików nie potwierdza fizycznego odczytu po zapisie. Po WRITE wykonaj READ BACK, porównaj wybrany zakres i potwierdź start konsoli.

## Zgłoszenie problemu

Podaj treść błędu, Windows, wersję Setup, J-Runnera, firmware, płytę i pamięć. Nie dołączaj CPU key ani prywatnych dumpów. To nadal szkic wydania przed końcowym testem sprzętowym.
