---
title: 'Dcm Dcm'
description: 'Dcm (BSW). Public interface of DCM for other components * * \details MICROSAR DCM based on AR 4.0.3'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Public interface of DCM for other components * * \details MICROSAR DCM based on AR 4.0.3

*Repository path:* `Dcm/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 14 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `Dcm.c`, `Dcm_Ext.c` |
| `include/` (12 header(s)) | `Dcm.h`, `Dcm_Cbk.h`, `Dcm_Core.h`, `Dcm_CoreCbk.h`, `Dcm_CoreInt.h`, `Dcm_CoreTypes.h`, `Dcm_Ext.h`, `Dcm_ExtCbk.h`, `Dcm_ExtInt.h`, `Dcm_ExtTypes.h`, `Dcm_Int.h`, `Dcm_Types.h` |
| `autosar/` (4 ARXML) | `Dcm_Dem430_preu.arxml`, `Dcm_SafeBSW_pre.arxml`, `Dcm_bswmd.arxml`, `Dcm_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `diagnostic`
- `Dcm_GetVersionInfo`
- `Dcm_GetActiveProtocol`
- `Dcm_GetTesterSourceAddress`
- `Dcm_ProcessVirtualRequest`
- `Dcm_ComM_NoComModeEntered`
- `Dcm_ComM_SilentComModeEntered`
- `Dcm_ComM_FullComModeEntered`
- `Dcm_ProvideRxBuffer`
- `Dcm_RxIndication`
- `Dcm_ProvideTxBuffer`
- `Dcm_TxConfirmation`
- `Dcm_OnRequestDetection`
- `Dcm_StartOfReception`
- `Dcm_CopyRxData`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Dcm.h`
- `Rte_Dcm.h`
- `SchM_Dcm.h`
- `PduR_Dcm.h`
- `ComM_Dcm.h`
- `Dcm_Int.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Dcm](../dcm__technicalreference-dcm-pdf/)

Source files remain in the repository next to this documentation.

