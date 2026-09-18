---
title: 'PduR PduR'
description: 'PduR (BSW). Det Error IDs as reported to DET.'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Det Error IDs as reported to DET.

*Repository path:* `PduR/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 2 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PduR.c` |
| `include/` (1 header(s)) | `PduR.h` |
| `autosar/` (1 ARXML) | `PduR_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `PduR_GetConfigurationId`
- `PduR_Init`
- `PduR_InitMemory`
- `PduR_GetVersionInfo`
- `PduR_UpTransmit`
- `PduR_LoIfRxIndication`
- `PduR_LoIfTriggerTransmit`
- `PduR_LoIfTxConfirmation`
- `PduR_LoTpStartOfReception`
- `PduR_LoTpCopyRxData`
- `PduR_LoTpRxIndication`
- `PduR_LoTpCopyTxData`
- `PduR_LoTpTxConfirmation`
- `PduR_CancelReceive`
- `PduR_ChangeParameter`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `PduR.h`
- `SchM_PduR.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_PduR](../pdur__technicalreference-pdur-pdf/)

Source files remain in the repository next to this documentation.

