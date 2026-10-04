# Distribution audit — 0.9.1 Beta

| File / group | Owner / source | License | Modified? | Redistributed? | Solution |
|---|---|---|---|---|---|
| MODI Setup / patch engine | MODI | MIT; original notice included | Yes | Compiled binary | One-click offline installer |
| PicoFlasher, Program, MainForm, NandInfo, NandTools, Resources and selected Nand types | J-Runner with Extras + MODI | MIT; original notice included | Yes | Audited compiled IL only | User's pinned original receives patch |
| MODI logo / Build resource | MODI | MODI notice | Yes | Yes | Own resource entries only |
| Mono.Cecil 0.11.6 | Jb Evain / Novell | MIT | No | Embedded DLL | Include exact original MIT notice |
| WaveStream.cs / WaveNative.cs | Ianier Munoz | Personal use restriction / redistribution unresolved | No | No | Preserve user's original code locally |
| AudioWriters, WAVFile | Original upstream authors | Unclear | No | No | Preserve user's original code locally |
| RegistryUtilities | Active Computing | Unclear | No | No | Preserve user's original code locally |
| ZIP / DotNetZip | Original upstream authors | Not fully audited | No | No | Preserve user's original code locally |
| MySql.Data / LibUsbDotNet / Windows API Code Pack | Respective upstream projects | Not cleared for this package | No | No | Original embedded resources preserved byte-for-byte |
| Other original J-Runner resources and support files | Respective upstream authors | Mixed / not audited here | No | No | User retains official installation |
| MODI PicoFlasher firmware | Balázs Triszka + contributors + MODI | GPLv2 headers / inherited GPLv3 LICENSE discrepancy | Yes | Draft UF2 + separate matching source | Preserve both texts; provenance review remains open |
| Pico SDK / TinyUSB sources | Raspberry Pi / TinyUSB contributors | Original BSD / MIT notices | No | Matching firmware source archive | Preserve original archives and notices |
| Newlib / GCC runtime portions | Toolchain upstream | Original runtime notices / exception | No | Firmware + required notices | Compiler binaries excluded |

Unclear elements default to NO REDISTRIBUTION. The local patch audit checks protected method IL and original embedded third-party resource hashes. This table records distribution decisions, not a claim that the outstanding firmware license provenance review is resolved.
