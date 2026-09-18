---
title: 'Fee Fee_30_SmallSector'
description: 'Fee_30_SmallSector (BSW). FEE header file * * \details The Flash Flash Emulation abstracts from the device specific addressing scheme and segmenta'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

FEE header file * * \details The Flash Flash Emulation abstracts from the device specific addressing scheme and segmentation and * provides a virtual addressing scheme and segmentation to upper layers as well as a virtually * unlimited numb

*Repository path:* `Fee_30_SmallSector/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 27 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (13 C file(s)) | `Fee_30_SmallSector.c`, `Fee_30_SmallSector_BlockHandler.c`, `Fee_30_SmallSector_DatasetHandler.c`, `Fee_30_SmallSector_FlsCoordinator.c`, `Fee_30_SmallSector_InstanceHandler.c`, `Fee_30_SmallSector_Layer1_Read.c`, `Fee_30_SmallSector_Layer1_Write.c`, `Fee_30_SmallSector_Layer2_DatasetEraser.c`, `Fee_30_SmallSector_Layer2_InstanceFinder.c`, `Fee_30_SmallSector_Layer2_WriteInstance.c`, `Fee_30_SmallSector_Layer3_ReadManagementBytes.c`, `Fee_30_SmallSector_PartitionHandler.c` |
| `include/` (14 header(s)) | `Fee_30_SmallSector.h`, `Fee_30_SmallSector_BlockHandler.h`, `Fee_30_SmallSector_Cbk.h`, `Fee_30_SmallSector_DatasetHandler.h`, `Fee_30_SmallSector_FlsCoordinator.h`, `Fee_30_SmallSector_InstanceHandler.h`, `Fee_30_SmallSector_Layer1_Read.h`, `Fee_30_SmallSector_Layer1_Write.h`, `Fee_30_SmallSector_Layer2_DatasetEraser.h`, `Fee_30_SmallSector_Layer2_InstanceFinder.h`, `Fee_30_SmallSector_Layer2_WriteInstance.h`, `Fee_30_SmallSector_Layer3_ReadManagementBytes.h` |
| `autosar/` (2 ARXML) | `Fee_30_SmallSector_SafeBSW_pre_Asr4.0.3.arxml`, `Fee_30_SmallSector_bswmd_Asr4.0.3.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Fee_30_SmallSector_Init`
- `Fee_30_SmallSector_Read`
- `Fee_30_SmallSector_Write`
- `Fee_30_SmallSector_InvalidateBlock`
- `Fee_30_SmallSector_EraseImmediateBlock`
- `Fee_30_SmallSector_Cancel`
- `Fee_30_SmallSector_GetStatus`
- `Fee_30_SmallSector_GetJobResult`
- `Fee_30_SmallSector_GetVersionInfo`
- `Fee_30_SmallSector_SetMode`
- `Fee_30_SmallSector_SuspendWrites`
- `Fee_30_SmallSector_ResumeWrites`
- `Fee_30_SmallSector_MainFunction`
- `Fee_30_SmallSector_AlignValue`
- `Fee_30_SmallSector_Bh_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Fee_30_SmallSector.h`
- `Fee_30_SmallSector_Cbk.h`
- `Fee_30_SmallSector_TaskManager.h`
- `Fee_30_SmallSector_FlsCoordinator.h`
- `Fee_30_SmallSector_PartitionHandler.h`
- `Fee_30_SmallSector_BlockHandler.h`
- `Fee_30_SmallSector_DatasetHandler.h`
- `Fee_30_SmallSector_Layer1_Read.h`
- `Fee_30_SmallSector_Layer1_Write.h`
- `Fee_30_SmallSector_Layer2_WriteInstance.h`
- `Fee_30_SmallSector_Layer2_DatasetEraser.h`
- `Fee_30_SmallSector_Layer2_InstanceFinder.h`
- `Fee_30_SmallSector_Layer3_ReadManagementBytes.h`
- `MemMap.h`
- `Fee_30_SmallSector_InstanceHandler.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Fee_30_SmallSector](../fee_30_smallsector__technicalreference-fee-30-smallsector-pdf/)

Source files remain in the repository next to this documentation.

