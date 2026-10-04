# MODI FLASHSHIP — Co dalej

[English](FLASHSHIP.md)

MODI FLASHSHIP to wspólna nazwa roadmapy kolejnych możliwości MODI Pico 2 Flasher X360 TURBO.

Roadmapa jest celowo oddzielona od wersji Stable. Funkcje przyszłościowe nie mogą opóźniać ani destabilizować pewnej obsługi NAND/eMMC.

## 🔜 Audio / Sonus — COMING SOON

Planowana obsługa audio/Sonus przy użyciu tego samego sprzętu MODI.

**Status:** trwają testy sprzętowe.

Nie traktować obecnego planu GPIO jako finalnego, dopóki nie zostanie sprawdzony na realnym sprzęcie. Wcześniejszy plan deweloperski używał GP11–GP15, ale GP11 uczestniczył również w pracach PIO / RDY-BSY. Przed publikacją finalnego pinoutu trzeba ponownie sprawdzić konflikty GPIO i aktualną alokację PIO.

## 💡 DirtyJTAG / Programowanie glitch chipów — PLANNED

Przyszłościowa możliwość programowania zewnętrznych glitch chipów z tego samego sprzętu RP2350.

Potencjalne urządzenia: Matrix, CoolRunner, ACE, Squirt i zgodne urządzenia JTAG.

Potencjalne protokoły: JTAG, SVF i XSVF.

## 💡 UART / COM Monitor — PLANNED

Przyszłościowa komunikacja szeregowa i funkcje diagnostyczne na tej samej platformie sprzętowej.

## 🔬 Diagnostyka HANA — RESEARCH

Przyszłe badania nad diagnostyką HANA w Xbox 360 i możliwymi workflow serwisowymi.

## 🧩 Natywne wsparcie w upstream J-Runner — PROPOSED

Jeżeli MODI okaże się stabilne na szerszej liczbie rewizji płyt, długoterminowym celem jest zaproponowanie opcjonalnego natywnego wsparcia MODI Pico 2 maintainerom J-Runner with Extras.

To wyłącznie propozycja. MODI nie sugeruje, że upstream zaakceptował lub oficjalnie wspiera ten projekt.

## Najpierw Stable

Aktualne priorytety pozostają bez zmian:

- pewne wykrywanie urządzenia,
- czysta integracja z J-Runnerem,
- szybkie i zweryfikowane operacje NAND/eMMC,
- czytelna dokumentacja,
- bezpieczna publiczna dystrybucja.
