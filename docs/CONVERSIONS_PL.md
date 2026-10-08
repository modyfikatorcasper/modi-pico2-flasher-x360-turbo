# ULTIMATE MEMORY CONVERSIONS

[English](CONVERSIONS.md) · [ULTIMATE](ULTIMATE_PL.md)

**IN DEVELOPMENT — brak działającej konwersji one-click**

Cel: obraz pod fizyczną wymianę pamięci na NAND 16 MB. Samo firmware nie zmienia układu, magistrali ani strapów płyty. Nie obcinamy pliku źródłowego.

| Rodzina źródłowa | Cel | Status / wymagania |
|---|---|---|
| Corona V2 4 GB | 16 MB NAND | IN DEVELOPMENT; osobna walidacja rewizji, eMMC i targetu |
| Corona V4 4 GB | 16 MB NAND | IN DEVELOPMENT; osobna walidacja rewizji, eMMC i targetu |
| Pozostałe warianty Corona eMMC | 16 MB NAND | IN DEVELOPMENT; wykrycie modelu/pojemności i lista zgodnych układów |
| Winchester 4 GB | 16 MB NAND | IN DEVELOPMENT; CPU Key i wymagane dane z obsługiwanej metody; brak klasycznego RGH |
| Jasper BB 256 MB | 16 MB NAND | IN DEVELOPMENT; geometria BB→SB, ECC i remapy |
| Jasper BB 512 MB | 16 MB NAND | IN DEVELOPMENT; geometria BB→SB, ECC i remapy |

## Docelowy workflow

`2 dumps → automatic compare → identify motherboard/memory → CPU Key → extract console data → build target image → hardware instructions → flash → full readback → verify → backup report`

Rozpoznanie ma ograniczać ręczny wybór parametrów. Każda rewizja musi mieć potwierdzone: target, połączenia i konfigurację sprzętową, boot chain/SMC, KV/config, rozmiar/spare/ECC i obsługę bad blocków. Brak klucza, niespójne odczyty lub nieobsługiwany target zatrzymują przygotowanie. Oryginalne dumpy pozostają zachowane; zapis sprzętu wymaga potwierdzenia fizycznego targetu.

## Winchester

CPU Key / wymagane dane muszą pochodzić z obsługiwanej metody, np. Bad Update z odpowiednim narzędziem do pozyskania danych. Nie obiecujemy jeszcze automatycznej obsługi tego procesu ani konwersji Winchester. Bad Update jest odrębnym, nietrwałym exploitem programowym; autor potwierdza działanie na Winchester. To nie jest klasyczne RGH. [Bad Update — original author](https://github.com/grimdoomer/Xbox360BadUpdate#faq).

## Walidacja przed udostępnieniem

Dwie niezależne zgodne kopie; testy poprawnych i błędnych obrazów; niezależny parser/validator; pełny zapis i identyczny readback; rzeczywisty start konsoli dla każdej zatwierdzonej kombinacji. Status pozostaje IN DEVELOPMENT do zaliczenia tych bramek.
