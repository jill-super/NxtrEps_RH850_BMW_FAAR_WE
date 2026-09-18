---
title: 'Os Os'
description: 'Os (OS). This file contains all data types which are exposed to the user. * \trace SPEC-63736'
---

:::tip[Origin: Vector-provided · MICROSAR]
Project-configured/generated for this ECU (DaVinci/MICROSAR tooling).
:::

## Purpose

This file contains all data types which are exposed to the user. * \trace SPEC-63736

*Repository path:* `Os/` · *AUTOSAR layer:* [Operating System (OS)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 220 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (44 C file(s)) | `Os_AccessCheck.c`, `Os_Alarm.c`, `Os_Application.c`, `Os_Barrier.c`, `Os_Bit.c`, `Os_BitArray.c`, `Os_Core.c`, `Os_Counter.c`, `Os_Deque.c`, `Os_Error.c`, `Os_Event.c`, `Os_Fifo.c` |
| `include/` (176 header(s)) | `Os.h`, `OsInt.h`, `Os_AccessCheck.h`, `Os_AccessCheckInt.h`, `Os_AccessCheck_Types.h`, `Os_Alarm.h`, `Os_AlarmInt.h`, `Os_Alarm_Types.h`, `Os_Application.h`, `Os_ApplicationInt.h`, `Os_Application_Types.h`, `Os_Barrier.h` |
| `autosar/` (3 ARXML) | `Os_Rh850_bswmd.arxml`, `Os_Rh850_bswmd_pre.arxml`, `Os_Rh850_bswmd_rec.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Os_GetVersionInfo`
- `Os_GetExceptionContext`
- `Os_SetExceptionContext`
- `Os_InitMemory`
- `Os_Init`
- `Os_EnterPreStartTask`
- `StartCore`
- `StartNonAutosarCore`
- `GetCoreID`
- `GetNumberOfActivatedCores`
- `GetActiveApplicationMode`
- `StartOS`
- `ShutdownOS`
- `ShutdownAllCores`
- `ControlIdle`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Std_Types.h`
- `Os_AccessCheck_Lcfg.h`
- `Os_AccessCheck.h`
- `Os_Common_Types.h`
- `Os_Thread.h`
- `Os_Isr.h`
- `Os_Task.h`
- `Os_Hal_Compiler.h`
- `Os_MemMap_OsCode.h`
- `Os_Alarm.h`
- `Os_Alarm_Lcfg.h`
- `Os_Counter.h`
- `Os_Event.h`
- `Os_Error.h`
- `Os_XSignal.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [AN-ISC-8-1166_RTE_BRE_without_AUTOSAR_OS](../os__an-isc-8-1166-rte-bre-without-autosar-os-pdf/)
- [TechnicalReference_Os](../os__technicalreference-os-pdf/)

Source files remain in the repository next to this documentation.

