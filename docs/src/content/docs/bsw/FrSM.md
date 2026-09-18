---
title: 'FrSM FrSM'
description: 'FrSM (BSW). Public header of the FlexRay State Manager AUTOSAR Release 4'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Public header of the FlexRay State Manager AUTOSAR Release 4

*Repository path:* `FrSM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `FrSM.c` |
| `include/` (2 header(s)) | `FrSM.h`, `FrSM_Types.h` |
| `autosar/` (2 ARXML) | `FrSM_bswmd.arxml`, `FrSM_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FrSM_InitMemory`
- `FrSM_Init`
- `FrSM_RequestComMode`
- `FrSM_GetCurrentComMode`
- `FrSM_GetVersionInfo`
- `FrSM_AllSlots`
- `FrSM_SetEcuPassive`
- `FrSM_MapNetworkHandleToLocalIndex`
- `FrSM_HandleComModeRequest`
- `FrSM_DetermineWakeupReason`
- `FrSM_TimerTriggeredTransitions`
- `FrSM_StateWakeup`
- `FrSM_StateStartOnline`
- `FrSM_RunTimer`
- `FrSM_StateReady`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `BswM_FrSM.h`
- `ComM.h`
- `ComM_BusSM.h`
- `SchM_FrSM.h`
- `FrIf.h`
- `FrSM.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_FrSM](../frsm__technicalreference-frsm-pdf/)

Source files remain in the repository next to this documentation.

