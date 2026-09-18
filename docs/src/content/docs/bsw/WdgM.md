---
title: 'WdgM WdgM'
description: 'WdgM (BSW). Header file containing prototype for Nexteer created WdgM Init function trusted function interface'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Header file containing prototype for Nexteer created WdgM Init function trusted function interface

*Repository path:* `WdgM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 2 file(s), vector: 7 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `NxtrWdgM.c`, `WdgM.c`, `WdgM_Checkpoint.c` |
| `include/` (3 header(s)) | `NxtrWdgM.h`, `WdgM.h`, `WdgM_Cfg.h` |
| `autosar/` (2 ARXML) | `WdgM_bswmd.arxml`, `WdgM_preo.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `NxtrWdgM_Init`
- `WdgM_Init`
- `WdgM_GetVersionInfo`
- `WdgM_CheckpointReached`
- `WdgM_SetMode`
- `WdgM_GetMode`
- `WdgM_GetLocalStatus`
- `WdgM_GetGlobalStatus`
- `WdgM_PerformReset`
- `WdgM_DeactivateSupervisionEntity`
- `WdgM_ActivateSupervisionEntity`
- `WdgM_UpdateTickCount`
- `WdgM_MainFunction`
- `WdgM_GetFirstExpiredSEID`
- `WdgM_GetFirstExpiredSEViolation`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Std_Types.h`
- `NxtrWdgM.h`
- `WdgM.h`
- `WdgM_PBcfg.h`
- `MemMap.h`
- `WdgIf.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_WdgM](../wdgm__technicalreference-wdgm-pdf/)

Source files remain in the repository next to this documentation.

