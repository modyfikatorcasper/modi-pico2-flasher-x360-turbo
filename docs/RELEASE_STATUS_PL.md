# Stan wydania — 0.9.1 Beta (szkic)

Instalator offline i jeden ZIP są gotowe. Test w świeżym folderze przeszedł: weryfikacja oryginału, instalacja bez jego podmiany, ponowny start oraz odrzucanie niezgodnych plików i niepełnej paczki. 753 metody odpowiadają sprawdzonej wersji; 18 testów integracji bez sprzętu przeszło. Firmware pozostaje niezmieniony.

Końcowa aplikacja jest uruchomiona i wykrywa podłączone Pico jako MODI Turbo. Odczyt, zapis, kontrola po zapisie i start konsoli na dokładnej paczce oraz prawdziwy screenshot nadal czekają. Przechwytywanie okna zwróciło timeout; nie zastępujemy zrzutu renderem testowym. Nie wykonano nowego zapisu ani odczytu konsoli na tej paczce.

Nowy szkic v0.9.1-beta jest na GitHub. Hashe wszystkich czterech plików binarnych/archiwów zgadzają się z lokalnymi. Publikacja GitHub Pages jest osobno zablokowana: strona nie jest włączona, a automat nie ma prawa jej włączyć. Właściciel musi włączyć Pages ze źródłem GitHub Actions.

[Pliki, hashe i pełny status](RELEASE_STATUS.md) · [Audyt dystrybucji](DISTRIBUTION_AUDIT.md).
