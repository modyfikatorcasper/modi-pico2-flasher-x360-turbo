# MODI FLASHSHIP — What's Next

[Polski](FLASHSHIP_PL.md)

MODI FLASHSHIP is the roadmap umbrella for future capabilities of MODI Pico 2 Flasher X360 TURBO.

It is intentionally separate from the current Stable release. Roadmap items must not delay or destabilize reliable NAND/eMMC service functionality.

## 🔜 Audio / Sonus — COMING SOON

Planned audio/Sonus support using the same MODI hardware.

**Status:** hardware testing in progress.

Do not treat the current GPIO plan as final until it is validated on real hardware. Earlier development planning used GP11–GP15, while GP11 has also been involved in PIO / RDY-BSY work. GPIO conflicts and current PIO allocation must be re-checked before a public pinout is declared final.

## 💡 DirtyJTAG / Glitch Chip Programmer — PLANNED

Future possibility: external glitch-chip programming from the same RP2350 hardware.

Potential target devices include Matrix, CoolRunner, ACE, Squirt and compatible JTAG devices.

Potential protocols include JTAG, SVF and XSVF.

## 💡 UART / COM Monitor — PLANNED

Future serial communication / diagnostic functionality using the same hardware platform.

## 🔬 HANA Diagnostics — RESEARCH

Future research into Xbox 360 HANA-related diagnostics and service workflows.

## 🧩 Native J-Runner upstream support — PROPOSED

If MODI proves stable across a broader set of hardware revisions, the long-term goal is to propose optional native MODI Pico 2 support to the J-Runner with Extras upstream maintainers.

This is only a proposal. MODI does not claim or imply upstream acceptance or endorsement.

## Stable first

The current priority remains:

- reliable device detection,
- clean J-Runner integration,
- fast verified NAND/eMMC service operations,
- clear documentation,
- safe public distribution.
