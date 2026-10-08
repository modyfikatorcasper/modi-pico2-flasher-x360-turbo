# MODI FLASHSHIP and pre-final status

[Polski](FLASHSHIP_PL.md)

The local pre-final contains built Audio/Sonus, DirtyJTAG and LIVE UART/HANA previews with XeLL LAN panels. New modules passed offline tests and need physical validation. The public NAND/eMMC v0.9.1-beta baseline retains its existing binaries.

[Package status and final 16 MB conversion milestone](PRE_FINAL.md) · [Wiring diagrams and connections](FLASHSHIP_WIRING.md)

## Audio Sonus

Digital ISD2100: GP12 MISO, GP13 SSB, GP14 SCLK, GP15 MOSI, **GP22 RDY/BSYB**, GND. Separate UF2 and MODI-Flashship companion. This does not target analog 5 V ISD1200 devices.

## DirtyJTAG

GP16 TDI, GP17 TDO, GP18 TCK, GP19 TMS, GND; GP20/21 optional resets. SVF/XSVF Xilinx programming path preview. ACE V3+ / V4 / V5 Gowin .fs needs a separate integration.

## LIVE UART HANA and XeLL

LIVE captures UART on GP9 and passive SMBus on GP10/GP11 concurrently. XeLL over LAN can run on the PC at the same time. Captured HANA traffic is not a full HDMI health test. Audio and DirtyJTAG remain separate profiles.

## Final planned development feature

Automatic image preparation for physical eMMC or Jasper 256/512 MB replacement with NAND 16 MB. Not implemented yet; scope and requirements are in the pre-final status.

## Upstream J-Runner support

Optional upstream integration remains a proposal. MODI does not imply maintainer acceptance or endorsement.
