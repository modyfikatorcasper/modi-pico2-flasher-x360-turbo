# Installation — MODI Pico 2 Flasher X360 TURBO

[Polski](INSTALL_PL.md)

## Requirements

Windows with .NET Framework 4.8, a complete official J-Runner with Extras 3.4.0.7 installation, and a Pico 2 / supported RP2350 board. Keep the upstream `common` and `xeBuild` folders next to `JRunner.exe`.

## Install

1. Download and extract `MODI-Pico2-Flasher-X360-TURBO-v0.9.1-beta.zip`.
2. Hold BOOTSEL while connecting the Pico 2 and copy the included UF2 to its exposed drive. Wait for reboot.
3. Run `MODI-Setup.exe`. Select a detected compatible installation or click **Wybierz JRunner.exe** to locate the official original once.
4. Click **Zainstaluj MODI TURBO**. Installation runs offline, verifies the exact original SHA256 and creates ready `JRunner.MODI.exe` next to the original.
5. Click **Uruchom MODI** or launch that executable directly.
6. Wire and power the console according to the correct motherboard service procedure. Confirm device and memory type, READ twice and compare before WRITE.

The installer interface is Polish. Original `JRunner.exe`, support files and third-party libraries remain in place. Setup does not require administrator privileges for a writable installation folder.

## Compatibility and repeat installation

Required original SHA256: `44F647B213B80489DBA0E396DDA262609BDF59D6F271DB416CDFE02507F8B39F`.

A repeated run verifies an identical MODI installation. It rejects an unsupported original, missing support folders, or a different existing `JRunner.MODI.exe`. To install alongside an older MODI edition, extract a fresh official J-Runner copy into another folder and select its original executable.

Keep `MODI-install-receipt.txt` next to the installed executable. Returning to stock means launching the unchanged original. Close both editions before switching.

## Verification

Check package SHA256. Always preserve a known-good backup. File comparison alone does not prove a physical post-write read-back. After WRITE, perform READ BACK and compare the selected range; confirm console boot.

## Reporting a problem

Include the error text, Windows version, Setup version, upstream version, firmware, motherboard and memory type. Do not attach CPU keys or private dumps. This release remains a draft pending final hardware QA.
