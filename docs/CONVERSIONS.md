# ULTIMATE MEMORY CONVERSIONS

[Polski](CONVERSIONS_PL.md) · [ULTIMATE](ULTIMATE.md)

**IN DEVELOPMENT — no working one-click conversion**

Goal: an image for physical memory replacement with a 16 MB NAND. Firmware alone cannot change the memory chip, bus or board straps. The source file is not blindly truncated.

| Source family | Target | Status / requirements |
|---|---|---|
| Corona V2 4 GB | 16 MB NAND | IN DEVELOPMENT; separate revision, eMMC and target validation |
| Corona V4 4 GB | 16 MB NAND | IN DEVELOPMENT; separate revision, eMMC and target validation |
| Other Corona eMMC variants | 16 MB NAND | IN DEVELOPMENT; model/capacity detection and target compatibility list |
| Winchester 4 GB | 16 MB NAND | IN DEVELOPMENT; CPU Key and required data from a supported method; no classic RGH |
| Jasper BB 256 MB | 16 MB NAND | IN DEVELOPMENT; BB→SB geometry, ECC and remaps |
| Jasper BB 512 MB | 16 MB NAND | IN DEVELOPMENT; BB→SB geometry, ECC and remaps |

## Target workflow

`2 dumps → automatic compare → identify motherboard/memory → CPU Key → extract console data → build target image → hardware instructions → flash → full readback → verify → backup report`

Detection should reduce manual parameter selection. Each revision needs validated target hardware, wiring/configuration, boot chain/SMC, KV/config, size/spare/ECC and bad-block handling. Missing keys, mismatched reads or unsupported targets stop preparation. Original dumps remain preserved; hardware writing requires confirmation of the physical target.

## Winchester

CPU Key / required data must come from a supported method, e.g. Bad Update with a suitable data-acquisition tool. Automatic acquisition and Winchester conversion are not promised as implemented. Bad Update is a separate, non-persistent software exploit; its author confirms Winchester support. It is not classic RGH. [Bad Update — original author](https://github.com/grimdoomer/Xbox360BadUpdate#faq).

## Validation before availability

Two independently matching backups; valid and invalid image fixtures; independent parser/validator; complete write and identical readback; real console boot for every approved combination. Status remains IN DEVELOPMENT until these gates pass.
