# MODI wiring diagrams

[English manual](../../docs/WIRING.md) · [Polski](../../docs/WIRING_PL.md)

Final PNGs are 2000 × 1500. They document the owner's actual seven-position Waveshare RP2350-Plus header with the existing MODI TURBO v0.9.1 pin assignment. Header position 3 is yellow GND; black GP3 is MOSI.

## References and image credits

- MODI owner's front and rear photographs: physical header order and actual wire colors.
- Matching v0.9.1 [corresponding firmware source](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip): `firmware-source/pins.h`, `xbox.c` and `emmc_fifo.c`.
- [15432/PicoFlasher](https://github.com/15432/PicoFlasher): GP0–GP5 SPI implementation and [original Corona reference](https://github.com/15432/PicoFlasher/blob/master/IMG_20241128_201825_526.jpg) / WORIKSTER.
- [xFlasher 360 User Guide v1.2 — Element18592](https://themodshop.co/xFlasher_360_User_Guide.pdf): SPI wire-to-pad table (page 6) and Trinity motherboard photograph. Only its SPI section is used here.
- [Weekend Modder / PicoFlasher](https://weekendmodder.com/picoflasher): motherboard wiring cross-check.
- [James Ledger — Fat NAND-X reference image](https://jamesledger.org/assets/images/jtag-2021/nandxphat-1.jpg): common Fat solder-area photograph; original NAND-X diagram credit retained.
- [Falcon schematic](https://xbox360hub.com/wp-content/uploads/2021/02/Xbox_360_Falcon_Schematic.pdf): J1D2 / J2B1 header identification.

Motherboard photography belongs to the credited sources. MODI adds the wiring overlay and tables. The RP2350-Plus insert is an AI-assisted cutout based on the owner's photograph; electrical mapping was checked against the original photographs and firmware, not generated labels. These diagrams document the existing build; they do not constitute a new hardware test.

## Asset integrity (SHA256)

```text
A4168B3B4B50C58759C7DD20DAFDCC8672B7DA6896C583F442B7756180165E2D  wiring-corona-rp2350-plus.png
E50CC3E1AC4167D8ADE1C3327620FDE8A5BC7DBE2835B77D52344E57DE0F25F8  wiring-trinity-rp2350-plus.png
53C8EEB39D190E364C7CF471DDBF0B8DCCA563CB108B51B6FE9C4193DDEFA6CB  wiring-falcon-rp2350-plus.png
```
