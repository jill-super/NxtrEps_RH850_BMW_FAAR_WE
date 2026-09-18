---
title: 'FrTrcv FrTrcv_30_Tja1082'
description: 'FrTrcv_30_Tja1082 (BSW). MICROSAR FR Transceiver Driver * * \details FlexRay transceiver driver header file'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

MICROSAR FR Transceiver Driver * * \details FlexRay transceiver driver header file

*Repository path:* `FrTrcv_30_Tja1082/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `FrTrcv_30_Tja1082.c` |
| `include/` (2 header(s)) | `FrTrcv_30_Tja1082.h`, `FrTrcv_30_Tja1082_Cbk.h` |
| `autosar/` (2 ARXML) | `FrTrcv_30_Tja1082_bswmd.arxml`, `FrTrcv_SafeBSW_pre.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FrTrcv_30_Tja1082_InitMemory`
- `FrTrcv_30_Tja1082_Init`
- `FrTrcv_30_Tja1082_GetVersionInfo`
- `FrTrcv_30_Tja1082_SetTransceiverMode`
- `FrTrcv_30_Tja1082_GetTransceiverMode`
- `FrTrcv_30_Tja1082_GetTransceiverWUReason`
- `FrTrcv_30_Tja1082_ClearTransceiverWakeup`
- `FrTrcv_30_Tja1082_DisableTransceiverBranch`
- `FrTrcv_30_Tja1082_EnableTransceiverBranch`
- `FrTrcv_30_Tja1082_GetTransceiverError`
- `FrTrcv_30_Tja1082_CheckWakeupByTransceiver`
- `Appl_FrTrcv_30_Tja1082_Wait`
- `Appl_FrTrcv_30_Tja1082_ReportErrorStatusPreFailed`
- `Appl_FrTrcv_30_Tja1082_ReportErrorStatusPrePassed`
- `FrTrcv_30_Tja1082_GetTrcvState`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `FrTrcv_30_Tja1082.h`
- `FrTrcv_30_Tja1082_Cbk.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_FrTrcv_Tja1082](../frtrcv_30_tja1082__technicalreference-frtrcv-tja1082-pdf/)

Source files remain in the repository next to this documentation.

