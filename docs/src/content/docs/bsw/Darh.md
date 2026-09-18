---
title: 'Darh Darh'
description: 'Darh (BSW). BMW Diagnostic Address Handling (BAC diagnostic routing helper).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW Diagnostic Address Handling (BAC diagnostic routing helper).

*Repository path:* `Darh/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 24 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (12 C file(s)) | `Darh.c`, `Darh_ApplAdapter.c`, `Darh_ConcAdapter.c`, `Darh_DataServicesHandler.c`, `Darh_ErrMemAdapter.c`, `Darh_EvtDataChngdHandler.c`, `Darh_MgmtHandler.c`, `Darh_NvMAdapter.c`, `Darh_QueueHandler.c`, `Darh_ReadActivelyReportedDTCs.c`, `Darh_RoutineControl.c`, `Darh_UDSAdapter.c` |
| `include/` (12 header(s)) | `Darh.h`, `Darh_ApplAdapter.h`, `Darh_AssertAdapter.h`, `Darh_ConcAdapter.h`, `Darh_ErrMemAdapter.h`, `Darh_Internal.h`, `Darh_NvM.h`, `Darh_NvMAdapter.h`, `Darh_QueueHandler.h`, `Darh_ReadActivelyReportedDTCs.h`, `Darh_RoutineControl.h`, `Darh_UDSAdapter.h` |
| `autosar/` (2 ARXML) | `DarhClassic_paramdef.arxml`, `Darh_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `Darh_SetRoeSuspendedHandler`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Darh.h`
- `Darh_Internal.h`
- `Darh_Version.h`
- `Darh_Cfg.h`
- `Darh_AssertAdapter.h`
- `Darh_ConcAdapter.h`
- `Darh_ApplAdapter.h`
- `string.h`
- `Darh_MemMap.h`
- `Rte_Darh.h`
- `DarhClassic_Version.h`
- `DarhClassic_Cfg.h`
- `Darh_QueueHandler.h`
- `BUtil/PlatformTypes.h`
- `Darh_ReadActivelyReportedDTCs.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DarhClassic_IntegrationManual](../darh__darhclassic-integrationmanual-pdf/)
- [DarhClassic_ReleaseNotes](../darh__darhclassic-releasenotes-pdf/)
- [DarhClassic_RequirementsTable](../darh__darhclassic-requirementstable-pdf/)
- [DarhGeneric_ReleaseNotes](../darh__darhgeneric-releasenotes-pdf/)
- [DarhGeneric_RequirementsTable](../darh__darhgeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

