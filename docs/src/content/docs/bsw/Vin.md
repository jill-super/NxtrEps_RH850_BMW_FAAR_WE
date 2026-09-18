---
title: 'Vin Vin'
description: 'Vin (BSW). BMW VIN handling (BAC vehicle identification).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW VIN handling (BAC vehicle identification).

*Repository path:* `Vin/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 10 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (5 C file(s)) | `Vin.c`, `Vin_Com.c`, `Vin_Dlog.c`, `Vin_SIAdapter.c`, `Vin_Ssv.c` |
| `include/` (5 header(s)) | `Vin.h`, `Vin_Dlog.h`, `Vin_Helper.h`, `Vin_NvM.h`, `Vin_Ssv.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Vin_NotifyVinReceived`
- `Vin_NotifyVinSecurityUpdate`
- `Vin_GetEnvironment`
- `Vin_SwitchToSafeEnvironment`
- `Vin_GetCurrentVin`
- `Vin_CheckInternalVin`
- `Vin_SsvInit`
- `Vin_SsvOnComOn`
- `Vin_SsvMain`
- `Vin_SsvCheckMac`
- `Vin_RequestVin`
- `Vin_Init`
- `Vin_Run`
- `Vin_CheckForVinChange`
- `Vin_Main`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 12):

- `Vin.h`
- `Vin_Cfg.h`
- `Vin_Helper.h`
- `Vin_Dlog.h`
- `Vin_Ssv.h`
- `Std_Types.h`
- `Rte_Vin.h`
- `Vin_MemMap.h`
- `Rte_VinSIAdapter.h`
- `BUtil_ByteMask.h`
- `Vin_PBCfg.h`
- `BUtil_Assert.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [IntegrationManual_Vin](../vin__integrationmanual-vin-pdf/)
- [ModuleSpecification_Vin](../vin__modulespecification-vin-pdf/)
- [ReleaseNotes_Vin](../vin__releasenotes-vin-pdf/)
- [UserGuide_Vin](../vin__userguide-vin-pdf/)

Source files remain in the repository next to this documentation.

