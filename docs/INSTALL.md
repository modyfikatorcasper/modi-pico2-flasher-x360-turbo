# Installation — MODI Pico 2 Flasher X360 TURBO

[Polski](INSTALL_PL.md)

## Requirements

- Windows x64
- .NET Framework 4.8
- compatible J-Runner with Extras 3.4.0.7 installation
- Raspberry Pi Pico 2 / compatible RP2350 board
- matching `MODI-Pico2-Flasher-X360-TURBO.uf2`
- correct wiring and service points for the target Xbox 360 motherboard
- Internet connection during the first MODI Setup run

## 1. Flash the Pico 2

1. Disconnect the Pico 2 from USB.
2. Hold **BOOTSEL**.
3. Connect USB while holding BOOTSEL.
4. Release the button when the USB drive appears.
5. Copy `MODI-Pico2-Flasher-X360-TURBO.uf2` to the exposed drive.
6. The board will reboot automatically into MODI firmware.

Always use the UF2 matching the documentation/release and verify its SHA256 before use.

## 2. Prepare J-Runner

MODI Setup **does not overwrite** the original `JRunner.exe`.

1. Download `MODI-Setup.exe` from GitHub Releases.
2. Run the installer.
3. Select an existing compatible J-Runner with Extras 3.4.0.7 `JRunner.exe`.
4. The installer validates the required version and files.
5. On first run it downloads the pinned build components it needs.
6. A private .NET SDK is used locally; MODI Setup does not change the global PATH.
7. When finished, `JRunner.MODI.exe` is created next to the original.

The original `JRunner.exe` remains unchanged.

## 3. First launch

1. Run `JRunner.MODI.exe`.
2. Connect MODI Pico 2 Flasher X360 TURBO.
3. Confirm that the device is identified as MODI.
4. Confirm the detected memory/flash type before any operation.

## 4. Most important rule

**Always READ and create a backup first.**

Recommended workflow:

1. READ / backup 1
2. READ / backup 2 where the selected J-Runner workflow expects it
3. COMPARE / VERIFY the dump files
4. only then WRITE
5. after writing, perform a read-back / compare when required by the service workflow

A file `VERIFY`/compare result does not necessarily mean that an automatic physical read-back was performed after WRITE.

## 5. Cache and logs

MODI Setup uses `%LOCALAPPDATA%\MODI\Setup\`.

Typical locations:

- cache: `%LOCALAPPDATA%\MODI\Setup\downloads`
- run log: `%LOCALAPPDATA%\MODI\Setup\run-ID\setup.log`

## 6. Removing MODI

Because the original J-Runner is not overwritten, returning to stock is straightforward:

- close J-Runner,
- remove `JRunner.MODI.exe` if you no longer want to use it,
- optionally remove MODI Setup cache / receipt files,
- launch the original `JRunner.exe` again.

## 7. Safety

- do not write an unverified NAND/eMMC image,
- do not publicly share CPU keys or private dumps,
- verify SHA256 for downloaded files,
- make and verify a known-good backup before WRITE,
- incorrect wiring or power can damage hardware.

## 8. Reporting an installation problem

Keep `setup.log` and include:

- Windows version,
- MODI Setup version,
- J-Runner version,
- MODI firmware version,
- Xbox 360 motherboard,
- flash type,
- stage where the failure occurred.

Do not attach private NAND dumps or CPU keys.
