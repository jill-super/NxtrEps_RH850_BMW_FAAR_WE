---
title: 'Xcp Xcp'
description: 'Xcp (BSW). XCP header file * * \details Header of the XCP protocol layer. * XCP V1.1 slave device driver'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

XCP header file * * \details Header of the XCP protocol layer. * XCP V1.1 slave device driver

*Repository path:* `Xcp/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 6 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Xcp.c` |
| `include/` (3 header(s)) | `Xcp.h`, `Xcp_Priv.h`, `Xcp_Types.h` |
| `autosar/` (3 ARXML) | `Xcp_SafeBSW_pre.arxml`, `Xcp_bswmd.arxml`, `Xcp_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Xcp_InitMemory`
- `Xcp_Init`
- `Xcp_GetVersionInfo`
- `Xcp_GetSessionStatus`
- `Xcp_SetActiveTl`
- `Xcp_GetActiveTl`
- `Xcp_TlRxIndication`
- `Xcp_TlTxConfirmation`
- `Xcp_Disconnect`
- `Xcp_ModifyProtectionStatus`
- `Xcp_StimEventStatus`
- `Xcp_Event`
- `Xcp_SendCrm`
- `Xcp_SendEvent`
- `Xcp_PutChar`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Xcp.h`
- `Xcp_Priv.h`
- `SchM_Xcp.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_XCP](../xcp__technicalreference-xcp-pdf/)
- [UserManual_AUTOSAR_Calibration](../xcp__usermanual-autosar-calibration-pdf/)
- [XCP_ReferenceBook_V3.0_EN](../xcp__xcp-referencebook-v3-0-en-pdf/)

Source files remain in the repository next to this documentation.

