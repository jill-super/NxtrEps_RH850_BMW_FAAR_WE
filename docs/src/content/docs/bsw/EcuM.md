---
title: 'EcuM EcuM'
description: 'EcuM (BSW). MICROSAR ECU State Manager * * \details This header provides some EcuM Callback Functions.'
---

:::tip[Origin: Vector-provided · MICROSAR]
Project-configured/generated for this ECU (DaVinci/MICROSAR tooling).
:::

## Purpose

MICROSAR ECU State Manager * * \details This header provides some EcuM Callback Functions.

*Repository path:* `EcuM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 4 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `EcuM.c` |
| `include/` (3 header(s)) | `EcuM.h`, `EcuM_Cbk.h`, `EcuM_Error.h` |
| `autosar/` (1 ARXML) | `EcuM_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `EcuM_Init`
- `EcuM_Shutdown`
- `EcuM_SelectShutdownTarget`
- `EcuM_GetShutdownTarget`
- `EcuM_GetLastShutdownTarget`
- `EcuM_SelectShutdownCause`
- `EcuM_GetShutdownCause`
- `EcuM_ClearWakeupEvent`
- `EcuM_ClearValidatedWakeupEvent`
- `EcuM_GetPendingWakeupEvents`
- `EcuM_GetValidatedWakeupEvents`
- `EcuM_GetExpiredWakeupEvents`
- `EcuM_StartCheckWakeup`
- `EcuM_EndCheckWakeup`
- `EcuM_GetBootTarget`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `EcuM.h`
- `EcuM_PrivateCfg.h`
- `BswM.h`
- `BswM_EcuM.h`
- `Rte_EcuM.h`
- `Rte_Main.h`
- `SchM_EcuM.h`
- `EcuM_Error.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_EcuM](../ecum__technicalreference-ecum-pdf/)

Source files remain in the repository next to this documentation.

