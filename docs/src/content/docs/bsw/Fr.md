---
title: 'Fr Fr'
description: 'Fr (BSW). FlexRay Driver header file * * \details Header file implementation of the AUTOSAR FlexRay Driver according to: * AUTOSAR'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

FlexRay Driver header file * * \details Header file implementation of the AUTOSAR FlexRay Driver according to: * AUTOSAR FlexRay Driver, AUTOSAR Release 4.0

*Repository path:* `Fr/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 7 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `Fr.c`, `Fr_Irq.c`, `Fr_Timer.c` |
| `include/` (4 header(s)) | `Fr.h`, `Fr_ERay.h`, `Fr_Ext.h`, `Fr_Priv.h` |
| `autosar/` (2 ARXML) | `Fr_V85xEray_SafeBSW_pre.arxml`, `Fr_V85xEray_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Fr_Init`
- `ApplFr_ISR_CycleStart`
- `ApplFr_ISR_CycleStart_1`
- `ApplFr_ISR_Timer0`
- `ApplFr_ISR_Timer0_1`
- `Fr_VIsMsgId`
- `Fr_VReadBackSupport`
- `Fr_VEnterConfigMode`
- `Fr_VLeaveConfigMode`
- `Fr_VExecutePOCCommand`
- `Fr_VBitCnt`
- `Fr_VSetReg`
- `Fr_VCalHeaderCRC`
- `Fr_VWriteDataToCC`
- `Fr_VReadDataFromCC`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Fr_Priv.h`
- `Std_Types.h`
- `MemMap.h`
- `Fr.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Fr](../fr__technicalreference-fr-pdf/)
- [TechnicalReference_Fr_V85x](../fr__technicalreference-fr-v85x-pdf/)

Source files remain in the repository next to this documentation.

