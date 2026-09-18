---
title: 'Dem Dem'
description: 'Dem (BSW). Implementation header file for the MICROSAR Dem * \details'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Implementation header file for the MICROSAR Dem * \details

*Repository path:* `Dem/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 187 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Dem.c` |
| `include/` (186 header(s)) | `Dem.h`, `Dem_API_Implementation.h`, `Dem_API_Interface.h`, `Dem_API_Types.h`, `Dem_Cbk.h`, `Dem_Cbk_Implementation.h`, `Dem_Cbk_Interface.h`, `Dem_Cbk_Types.h`, `Dem_Cdd_Types.h`, `Dem_Cfg_Declarations.h`, `Dem_Cfg_Definitions.h`, `Dem_Cfg_Macros.h` |
| `autosar/` (4 ARXML) | `Dem_Pre.arxml`, `Dem_SafeBSW_pre.arxml`, `Dem_bswmd.arxml`, `Dem_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Dem_MasterMainFunctionTimer`
- `Dem_MasterMainFunctionWorker`
- `Dem_InitMemory`
- `Dem_MainFunctionTimer`
- `Dem_MainFunctionWorker`
- `Dem_MainFunction`
- `Dem_SatellitePreInit`
- `Dem_MasterPreInit`
- `Dem_PreInit`
- `Dem_SatelliteInit`
- `Dem_MasterInit`
- `Dem_Init`
- `Dem_Shutdown`
- `Dem_MasterMainFunction`
- `Dem_SatelliteMainFunction`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Dem.h`
- `Dem_Cbk.h`
- `Dem_Int.h`
- `SchM_Dem.h`
- `Dem_Swc.h`
- `Dem_AdditionalIncludeCfg.h`
- `Dem_Cfg_Declarations.h`
- `Dem_Cfg_Definitions.h`
- `Dem_Error_Implementation.h`
- `Dem_API_Implementation.h`
- `Dem_DcmAPI_Implementation.h`
- `Dem_Memory_Implementation.h`
- `Dem_DataReportIF_Implementation.h`
- `Dem_DataStorageIF_Implementation.h`
- `Dem_Data_Implementation.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Dem](../dem__technicalreference-dem-pdf/)

Source files remain in the repository next to this documentation.

