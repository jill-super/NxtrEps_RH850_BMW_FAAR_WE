---
title: 'FrXcp FrXcp'
description: 'FrXcp (BSW). FlexRay XCP transport interface.'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

FlexRay XCP transport interface.

*Repository path:* `FrXcp/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 4 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `FrXcp.c` |
| `include/` (3 header(s)) | `FrXcp.h`, `FrXcp_Cbk.h`, `FrXcp_Types.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FrXcp_InitMemory`
- `FrXcp_Init`
- `FrXcp_TLService`
- `FrXcp_Send`
- `FrXcp_SendFlush`
- `FrXcp_DaqResumeStore`
- `FrXcp_DaqResumeClear`
- `XcpAppl_DaqTlResumeClear`
- `XcpAppl_DaqTlResumeStore`
- `XcpAppl_DaqTlResume`
- `FrXcp_GetVersionInfo`
- `FrXcp_MainFunctionRx`
- `FrXcp_MainFunctionTx`
- `FrXcp_SetPduMode`
- `Xcp_FrIfTxConfirmation`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `FrXcp.h`
- `FrXcp_Cbk.h`
- `Det.h`
- `FrIf.h`
- `SchM_Xcp.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_FrXcp](../frxcp__technicalreference-frxcp-pdf/)

Source files remain in the repository next to this documentation.

