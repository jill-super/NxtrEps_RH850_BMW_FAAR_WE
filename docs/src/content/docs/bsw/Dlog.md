---
title: 'Dlog Dlog'
description: 'Dlog (BSW). BMW diagnostic logger (Dlog) with shared generic part (DlogShared).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW diagnostic logger (Dlog) with shared generic part (DlogShared).

*Repository path:* `Dlog/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 35 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (15 C file(s)) | `Dlog_BootMode.c`, `Dlog_CodingAdapter.c`, `Dlog_Ecu.c`, `Dlog_Memory.c`, `Dlog_Mode.c`, `Dlog_NvMAdapter.c`, `Dlog_SvkGen.c`, `Dlog_Swe.c`, `Dlog_SweException.c`, `Dlog_SweGen.c`, `Dlog_SweGet.c`, `Dlog_SweInit.c` |
| `include/` (20 header(s)) | `Dlog.h`, `Dlog_BluSweCheckSum.h`, `Dlog_BootMode.h`, `Dlog_CodingAdapter.h`, `Dlog_Data.h`, `Dlog_Ecu.h`, `Dlog_Memory.h`, `Dlog_NvMAdapter.h`, `Dlog_Rte2C.h`, `Dlog_SvkGen.h`, `Dlog_Swe.h`, `Dlog_SweException.h` |
| `autosar/` (2 ARXML) | `DlogClassic_paramdef.arxml`, `Dlog_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `Dlog_GetVin`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Dlog_BootMode.h`
- `DlogClassic_Cfg.h`
- `Dlog_MemMap.h`
- `Dlog_CodingAdapter.h`
- `Rte_Dlog.h`
- `Dlog_Ecu.h`
- `Dlog_PBCfg.h`
- `Dlog_Nvm.h`
- `Dlog_Swe.h`
- `Dlog_HweTable.h`
- `Dlog_Data.h`
- `Dlog_Rte2C.h`
- `BUtil_ByteMask.h`
- `Dlog_Memory.h`
- `Dlog_User.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DlogClassic_IntegrationManual](../dlog__dlogclassic-integrationmanual-pdf/)
- [DlogClassic_ReleaseNotes](../dlog__dlogclassic-releasenotes-pdf/)
- [DlogClassic_RequirementsTable](../dlog__dlogclassic-requirementstable-pdf/)
- [DlogGeneric_ReleaseNotes](../dlog__dloggeneric-releasenotes-pdf/)
- [DlogGeneric_RequirementsTable](../dlog__dloggeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

