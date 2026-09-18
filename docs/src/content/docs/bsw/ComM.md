---
title: 'ComM ComM'
description: 'ComM (BSW). Communication Manager ASR4 * * \details Header of the Autosar Communication Manager'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Communication Manager ASR4 * * \details Header of the Autosar Communication Manager

*Repository path:* `ComM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 7 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `ComM.c` |
| `include/` (6 header(s)) | `ComM.h`, `ComM_BusSM.h`, `ComM_Dcm.h`, `ComM_EcuMBswM.h`, `ComM_Nm.h`, `ComM_Types.h` |
| `autosar/` (1 ARXML) | `ComM_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `ComM_MainFunction`
- `ComM_Init`
- `ComM_InitMemory`
- `ComM_DeInit`
- `ComM_GetStatus`
- `ComM_GetState`
- `ComM_RequestComMode`
- `ComM_GetMaxComMode`
- `ComM_GetRequestedComMode`
- `ComM_GetCurrentComMode`
- `ComM_GetInhibitionStatus`
- `ComM_PreventWakeUp`
- `ComM_LimitChannelToNoComMode`
- `ComM_LimitECUToNoComMode`
- `ComM_ReadInhibitCounter`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `ComM_Private_Cfg.h`
- `BswM_ComM.h`
- `SchM_ComM.h`
- `ComM_EcuMBswM.h`
- `ComM_BusSM.h`
- `ComM_Nm.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_ComM](../comm__technicalreference-comm-pdf/)

Source files remain in the repository next to this documentation.

