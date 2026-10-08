# MODI FLASHSHIP i stan pre-final

[English](FLASHSHIP.md)

Lokalny pre-final zawiera gotowe buildy Audio/Sonus, DirtyJTAG oraz LIVE UART/HANA z panelem XeLL po LAN. Nowe moduły mają zaliczone testy offline i wymagają walidacji sprzętowej. Publiczna baza NAND/eMMC v0.9.1-beta zachowuje dotychczasowe binaria.

[Stan paczki i ostatnia funkcja konwersji do 16 MB](PRE_FINAL_PL.md) · [Diagramy i podłączenia](FLASHSHIP_WIRING_PL.md)

## Audio Sonus

Cyfrowe ISD2100: GP12 MISO, GP13 SSB, GP14 SCLK, GP15 MOSI, **GP22 RDY/BSYB**, GND. Osobny profil UF2 i panel MODI-Flashship. Nie dotyczy analogowego ISD1200 5 V.

## DirtyJTAG

GP16 TDI, GP17 TDO, GP18 TCK, GP19 TMS, GND; GP20/21 opcjonalne resety. Preview SVF/XSVF dla ścieżki Xilinx. ACE V3+ / V4 / V5 Gowin .fs potrzebują osobnej integracji.

## LIVE UART HANA i XeLL

LIVE odbiera jednocześnie UART na GP9 i pasywny SMBus na GP10/GP11. XeLL po LAN może działać równolegle na PC. Przechwycony ruch HANA nie stanowi pełnego testu sprawności HDMI. Audio i DirtyJTAG pozostają oddzielnymi profilami.

## Ostatnia planowana funkcja

Automatyczne przygotowanie obrazu pod fizyczną wymianę eMMC albo Jasper 256/512 MB na NAND 16 MB. Funkcja nie jest jeszcze zaimplementowana; zakres i wymagania są w opisie pre-final.

## Wsparcie upstream J-Runner

Opcjonalna integracja upstream pozostaje propozycją. MODI nie sugeruje akceptacji ani oficjalnego poparcia maintainerów.
