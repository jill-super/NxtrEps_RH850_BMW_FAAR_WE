---
title: 'NvM NvM'
description: 'NvM (BSW). Initializes component. * \details Service for basic NVRAM manager initialization: initializes internal structures and th'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Initializes component. * \details Service for basic NVRAM manager initialization: initializes internal structures and the state machines. * \context TASK * \reentrant FALSE * \synchronous TRUE * \pre - * \trace CREQ-723

*Repository path:* `NvM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 14 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (6 C file(s)) | `NvM.c`, `NvM_Act.c`, `NvM_Crc.c`, `NvM_JobProc.c`, `NvM_Qry.c`, `NvM_Queue.c` |
| `include/` (8 header(s)) | `NvM.h`, `NvM_Act.h`, `NvM_Cbk.h`, `NvM_Crc.h`, `NvM_JobProc.h`, `NvM_Qry.h`, `NvM_Queue.h`, `NvM_Types.h` |
| `autosar/` (1 ARXML) | `NvM_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `NvM_Init`
- `NvM_SetDataIndex`
- `NvM_GetDataIndex`
- `NvM_SetBlockProtection`
- `NvM_GetErrorStatus`
- `NvM_GetVersionInfo`
- `NvM_SetRamBlockStatus`
- `NvM_ReadBlock`
- `NvM_WriteBlock`
- `NvM_RestoreBlockDefaults`
- `NvM_EraseNvBlock`
- `NvM_InvalidateNvBlock`
- `NvM_CancelJobs`
- `NvM_ReadAll`
- `NvM_WriteAll`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 11):

- `Std_Types.h`
- `NvM.h`
- `NvM_PrivateCfg.h`
- `NvM_JobProc.h`
- `NvM_Act.h`
- `NvM_Qry.h`
- `NvM_Queue.h`
- `NvM_Crc.h`
- `NvM_Cbk.h`
- `MemMap.h`
- `NvM_Cfg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_NvM](../nvm__technicalreference-nvm-pdf/)

Source files remain in the repository next to this documentation.

