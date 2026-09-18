---
title: 'IpduM IpduM'
description: 'IpduM (BSW). Vendor and module identification of this implementation. \{'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Vendor and module identification of this implementation. \{

*Repository path:* `IpduM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `IpduM.c` |
| `include/` (2 header(s)) | `IpduM.h`, `IpduM_Cbk.h` |
| `autosar/` (3 ARXML) | `IpduM_SafeBSW_pre.arxml`, `IpduM_bswmd.arxml`, `IpduM_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `IpduM_Init`
- `IpduM_InitMemory`
- `IpduM_GetVersionInfo`
- `IpduM_Transmit`
- `IpduM_TriggerTransmit`
- `IpduM_TxConfirmation`
- `IpduM_RxIndication`
- `IpduM_CopySegments`
- `IpduM_JitUpdate`
- `IpduM_JitTriggerTransmit`
- `IpduM_ContainerWriteHeader`
- `IpduM_ContainerReadHeader`
- `IpduM_GetRxHeaderSize`
- `IpduM_GetTxHeaderSize`
- `IpduM_TransmitCurrContainerPdu`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `IpduM.h`
- `IpduM_Cbk.h`
- `SchM_IpduM.h`
- `vstdlib.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_IpduM](../ipdum__technicalreference-ipdum-pdf/)

Source files remain in the repository next to this documentation.

