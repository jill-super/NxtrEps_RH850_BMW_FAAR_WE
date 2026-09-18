---
title: 'FrTp FrTp'
description: 'FrTp (BSW). Header file of the FrTp main-module. * * \details Declares all API functions of the FrTp.'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Header file of the FrTp main-module. * * \details Declares all API functions of the FrTp.

*Repository path:* `FrTp/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 16 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (6 C file(s)) | `FrTp.c`, `FrTp_FrIf.c`, `FrTp_Rsrc.c`, `FrTp_RxSm.c`, `FrTp_TxSm.c`, `FrTp_Util.c` |
| `include/` (10 header(s)) | `FrTp.h`, `FrTp_Cbk.h`, `FrTp_Common.h`, `FrTp_FrIf.h`, `FrTp_Rsrc.h`, `FrTp_RxSm.h`, `FrTp_TxSm.h`, `FrTp_Types.h`, `FrTp_Util.h`, `FrTp_XCfg.h` |
| `autosar/` (4 ARXML) | `FrTp_SafeBSW_pre.arxml`, `SchM_FrTp_pre.arxml`, `Tp_Iso10681_bswmd.arxml`, `Tp_Iso10681_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FrTp_Init`
- `FrTp_Shutdown`
- `FrTp_Transmit`
- `FrTp_CancelTransmit`
- `FrTp_CancelReceive`
- `FrTp_ChangeParameter`
- `FrTp_GetVersionInfo`
- `FrTp_InitMemory`
- `FrTp_RxIndication`
- `FrTp_TxConfirmation`
- `FrTp_TriggerTransmit`
- `FrTp_FrIf_RxIndication`
- `FrTp_FrIf_ProcessTxConfirmations`
- `FrTp_FrIf_ResetTxPduPending`
- `FrTp_FrIf_IncreaseNumTxConfOverlapped`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `FrTp_Common.h`
- `FrTp_Cbk.h`
- `FrTp.h`
- `FrIf.h`
- `MemMap.h`
- `vstdlib.h`
- `PduR_FrTp.h`
- `FrTp_Util.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Asr_FrTp](../frtp__technicalreference-asr-frtp-pdf/)

Source files remain in the repository next to this documentation.

