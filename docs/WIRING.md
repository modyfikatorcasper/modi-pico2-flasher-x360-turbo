# MODI Pico 2 Flasher X360 TURBO — wiring / pinout

[Polski](WIRING_PL.md) · [Installation](INSTALL.md)

These diagrams are for the **Waveshare RP2350-Plus fitted with the pictured MODI header** and the published MODI TURBO v0.9.1 firmware. Wire colors come from the owner's real front/rear photographs. Other boards and cable assemblies may use different colors; match the GPIO labels and signals.

## Pinout / Header

These are the pins used by our **NAND/SPI header**.

| Header position¹ | Wire color | RP2350 pin | Signal | Corona / Trinity pad | Falcon / Fat pad |
|---:|---|---|---|---|---|
| 1 | Orange | GP0 | SPI_MISO | J2C1.4 | J1D2.4 |
| 2 | Brown | GP1 | SPI_SS_N | J2C1.2 | J1D2.2 |
| 3 | Yellow | GND | GND | J2C1.6 | J1D2.6 |
| 4 | Red | GP2 | SPI_CLK | J2C1.3 | J1D2.3 |
| 5 | Black | GP3 | SPI_MOSI | J2C1.1 | J1D2.1 |
| 6 | Blue | GP4 | SMC_DBG_EN | J2C3.6 | J2B1.6 |
| 7 | Green | GP5 | SMC_RST_XDK_N | J2C3.5 | J2B1.5 |

¹ Count down from the USB end of the pictured **seven-position MODI header**. With USB at the top, the header is on the **left when viewing the front** (components / BOOT / RESET) and on the **right when viewing the rear** (GPIO silkscreen).

Physical order: **GP0 → GP1 → GND → GP2 → GP3 → GP4 → GP5**.

**Yellow is GND. Black is SPI_MOSI.** GPIO numbers are not header-position numbers. The ground contact is between GP1 and GP2. `J2C1.4` means pad 4 of J2C1, not GPIO 4. Find pad 1 from the board marking / square pad and follow the pictured orientation; do not count using wire position alone.

## Corona — J2C1 + J2C3

![Corona wiring: motherboard pads to the seven-position RP2350-Plus MODI header](../assets/wiring/wiring-corona-rp2350-plus.png)

[Open full-size Corona diagram](../assets/wiring/wiring-corona-rp2350-plus.png)

The MODI build uses this **SPI route for Corona 16 MB NAND and Corona 4 GB eMMC**, through the console's flash interface. It does not use the stock PicoFlasher GP6–GP9 / direct U1D1 eMMC scheme. Do not mix those diagrams with this firmware. Check your Corona revision and continuity around the relevant service points, including R2C10 where applicable; the pictured layout is not an instruction to bridge an unidentified component.

## Trinity — J2C1 + J2C3

![Trinity wiring: motherboard pads to the seven-position RP2350-Plus MODI header](../assets/wiring/wiring-trinity-rp2350-plus.png)

[Open full-size Trinity diagram](../assets/wiring/wiring-trinity-rp2350-plus.png)

Match J2C1 and J2C3 labels and pad 1 orientation before soldering.

## Falcon / Fat — J1D2 + J2B1

![Falcon / Fat wiring: J1D2 and J2B1 pads to the RP2350-Plus MODI header](../assets/wiring/wiring-falcon-rp2350-plus.png)

[Open full-size Falcon / Fat diagram](../assets/wiring/wiring-falcon-rp2350-plus.png)

The table targets Falcon's J1D2 / J2B1 connections. The solder-area photograph is a **common Fat reference**, not an independently identified Falcon photograph. Confirm the actual motherboard revision, header labels and pad 1 on your console; other Fat boards require their own revision check.

## Before connecting

1. Identify the motherboard and memory type. Compare each colored wire with the official MODI diagram and the rear GPIO labels.
2. Disconnect console power and programmer USB while soldering. Check continuity, pad numbers and adjacent-pad shorts.
3. Keep wires short and secure. For a transfer, leave the console off with its PSU connected in standby; connect the programmer USB after checking the wiring.
4. Make two reads and compare them before writing. After writing, read back and compare the selected range.
5. Disconnect the programmer before booting the console.

## References and image credits

- MODI owner's front and rear photographs: physical header order and actual wire colors.
- Matching v0.9.1 [corresponding firmware source](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-SOURCE-v0.9.1.zip): `firmware-source/pins.h`, `xbox.c` and `emmc_fifo.c`.
- [15432/PicoFlasher](https://github.com/15432/PicoFlasher): GP0–GP5 SPI implementation and [original Corona reference](https://github.com/15432/PicoFlasher/blob/master/IMG_20241128_201825_526.jpg) / WORIKSTER.
- [xFlasher 360 User Guide v1.2 — Element18592](https://themodshop.co/xFlasher_360_User_Guide.pdf): SPI wire-to-pad table (page 6) and Trinity motherboard photograph. Only its SPI section is used here.
- [Weekend Modder / PicoFlasher](https://weekendmodder.com/picoflasher): motherboard wiring cross-check.
- [James Ledger — Fat NAND-X reference image](https://jamesledger.org/assets/images/jtag-2021/nandxphat-1.jpg): common Fat solder-area photograph; original NAND-X diagram credit retained.
- [Falcon schematic](https://xbox360hub.com/wp-content/uploads/2021/02/Xbox_360_Falcon_Schematic.pdf): J1D2 / J2B1 header identification.

Motherboard photography belongs to the credited sources. MODI adds the wiring overlay and tables. The RP2350-Plus insert is an AI-assisted cutout based on the owner's photograph; electrical mapping was checked against the original photographs and firmware, not generated labels. These diagrams document the existing build; they do not constitute a new hardware test.
