---
title: 'CM103A RamMem'
description: 'CM103A_RamMem_Impl (CDD). Declarations of global functions of CM103A RAM Memory'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Declarations of global functions of CM103A RAM Memory

*Repository path:* `CM103A_RamMem_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 15 file(s), renesas: 2 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_RamMem.c`, `CDD_RamMemNonRte.c` |
| `include/` (1 header(s)) | `CDD_RamMem.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `RamMemLclRamSngBitEcc`
- `SpiEccErr`
- `FrEccErr`
- `CanEccErr`
- `RamMemInit1`
- `RamMemPer1`
- `RamFailrModClassnChk`
- `RamMemLclRamFailrChk`
- `FuncForLclRamInstrFetchErrInj`
- `InjRamErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 12):

- `Rte_CDD_RamMem.h`
- `NxtrMath.h`
- `CDD_RamMem.h`
- `ecm_regs.h`
- `ecc_regs.h`
- `NxtrMcuSuprtLib.h`
- `dma_regs.h`
- `CDD_RamMem_MemMap.h`
- `Os.h`
- `CDD_ExcpnHndlg.h`
- `McuErrInj.h`
- `Spi.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [RamMem_Integration Manual](../cm103a_rammem_impl__rammem-integration-manual-doc/)
- [RamMem_MDD](../cm103a_rammem_impl__rammem-mdd-docx/)

Source files remain in the repository next to this documentation.

