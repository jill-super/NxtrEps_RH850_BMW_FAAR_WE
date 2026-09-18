---
title: 'CM102A FlsMem'
description: 'CM102A_FlsMem_Impl (CDD). Flash Memory Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Flash Memory Complex Driver Header

*Repository path:* `CM102A_FlsMem_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 17 file(s), renesas: 1 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_FlsMem.c`, `CDD_FlsMemNonRte.c` |
| `include/` (2 header(s)) | `CDD_FlsMem.h`, `CDD_FlsMemNonRte_MemMap.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `FlsMem_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 8):

- `DtsInin`
- `DtsClnUp`
- `FlsMemInit2`
- `CodFlsSngBitEcc`
- `FlsMemInit1`
- `FlsMemPer2`
- `AddressParityTestFunction`
- `InjCodFlsEccErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 14):

- `Rte_CDD_FlsMem.h`
- `CDD_FlsMem.h`
- `CDD_FlsMem_Cfg_private.h`
- `intc_regs.h`
- `dma_regs.h`
- `Os.h`
- `CDD_FlsMem_MemMap.h`
- `CDD_SyncCrc.h`
- `CDD_NxtrTi.h`
- `ecc_regs.h`
- `CDD_ExcpnHndlg.h`
- `NxtrMcuSuprtLib.h`
- `McuErrInj.h`
- `CDD_FlsMemNonRte_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [FlsMem Integration Manual](../cm102a_flsmem_impl__flsmem-integration-manual-doc/)
- [FlsMem Module Design Document](../cm102a_flsmem_impl__flsmem-module-design-document-docx/)

Source files remain in the repository next to this documentation.

