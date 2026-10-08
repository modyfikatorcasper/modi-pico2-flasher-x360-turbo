# Installation — MODI Pico 2 Flasher X360 TURBO

[Polski](INSTALL_PL.md)

## Requirements

Windows with .NET Framework 4.8, a complete official J-Runner with Extras 3.4.0.7 installation, and a Pico 2 / supported RP2350 board. Keep the upstream `common` and `xeBuild` folders next to `JRunner.exe`.

Flash [the Pico 2 UF2](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO.uf2), then download [the complete MODI ZIP](https://github.com/modyfikatorcasper/modi-pico2-flasher-x360-turbo/releases/download/v0.9.1-beta/MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip) and use the [official J-Runner 3.4.0 r7 base](https://github.com/J-Runner-With-Extras/J-Runner-with-Extras/releases/tag/V3.4.0-r7).

## Install

1. Download and extract `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip`.
2. Hold BOOTSEL while connecting the Pico 2 and copy the included UF2 to its exposed drive. Wait for reboot.
3. Run `MODI-Setup.exe`. Select a detected compatible installation or click **Wybierz JRunner.exe** to locate the official original once.
4. Click **Zainstaluj MODI TURBO**. Installation runs offline, verifies the exact original SHA256 and creates ready `JRunner.MODI.exe` next to the original.
5. Click **Uruchom MODI** or launch that executable directly.
6. Wire and power the console according to the correct motherboard service procedure. Confirm device and memory type, READ twice and compare before WRITE.

The installer interface is Polish. Original `JRunner.exe`, support files and third-party libraries remain in place. Setup does not require administrator privileges for a writable installation folder.

## Pinout / Header — MODI Pico 2 Flasher X360 TURBO

Our NAND/SPI header pins on Waveshare RP2350-Plus:

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

Diagrams and connection procedure: [Corona, Trinity and Falcon / Fat](WIRING.md).

## Compatibility and repeat installation

Required original SHA256: `44F647B213B80489DBA0E396DDA262609BDF59D6F271DB416CDFE02507F8B39F`.

A repeated run verifies an identical MODI installation. It rejects an unsupported original, missing support folders, or a different existing `JRunner.MODI.exe`. To install alongside an older MODI edition, extract a fresh official J-Runner copy into another folder and select its original executable.

Keep `MODI-install-receipt.txt` next to the installed executable. Returning to stock means launching the unchanged original. Close both editions before switching.

## Verification

Check package SHA256. Always preserve a known-good backup. File comparison alone does not prove a physical post-write read-back. After WRITE, perform READ BACK and compare the selected range; confirm console boot.

## Reporting a problem

Include the error text, Windows version, Setup version, upstream version, firmware, motherboard and memory type. Do not attach CPU keys or private dumps. This is the public 0.9.1 Beta; hardware tests were confirmed by the user on 2026-10-04.

## New pre-final modules

[Trinity and Corona Audio, plus ACE, CoolRunner and Matrix DirtyJTAG](FLASHSHIP_WIRING.md) · [Status and final 16 MB conversion milestone](PRE_FINAL.md)

New connections use separate preview profiles. Audio RDY is GP22. Hardware validation of new modules is pending; the public installer still provides the tested v0.9.1-beta baseline.
