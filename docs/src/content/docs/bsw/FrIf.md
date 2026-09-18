---
title: 'FrIf FrIf'
description: 'FrIf (BSW). FlexRay Interface header file * * \details Header file implementation of the AUTOSAR FlexRay Interface according to: * A'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

FlexRay Interface header file * * \details Header file implementation of the AUTOSAR FlexRay Interface according to: * AUTOSAR FlexRay Interface, AUTOSAR Release 4.0

*Repository path:* `FrIf/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 10 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (6 C file(s)) | `FrIf.c`, `FrIf_AbsTimer.c`, `FrIf_Rx.c`, `FrIf_Time.c`, `FrIf_Trcv.c`, `FrIf_Tx.c` |
| `include/` (4 header(s)) | `FrIf.h`, `FrIf_Cbk.h`, `FrIf_Ext.h`, `FrIf_Priv.h` |
| `autosar/` (3 ARXML) | `FrIf_SafeBSW_pre.arxml`, `FrIf_bswmd.arxml`, `FrIf_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FrIf_InitMemory`
- `FrIf_Init`
- `FrIf_MainFunction`
- `FrIf_MainFunction_0`
- `FrIf_MainFunction_1`
- `FrIf_SetState`
- `FrIf_GetState`
- `FrIf_GetMacroticksPerCycle`
- `FrIf_GetMacrotickDuration`
- `FrIf_JobListExec`
- `FrIf_JobListExec_0`
- `FrIf_JobListExec_1`
- `FrIf_CancelTransmit`
- `FrIf_GetVersionInfo`
- `FrIf_Transmit`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `FrIf_Priv.h`
- `MemMap.h`
- `FrIf_Cbk.h`
- `vstdlib.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [AN-ISC-8-1140_FrIf_JobListConfiguration](../frif__an-isc-8-1140-frif-joblistconfiguration-pdf/)
- [TechnicalReference_FrIf](../frif__technicalreference-frif-pdf/)

Source files remain in the repository next to this documentation.

