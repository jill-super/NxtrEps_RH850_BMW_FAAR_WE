---
title: 'MemIf MemIf'
description: 'MemIf (BSW). Memory Interface header file * * \details The Memory Abstraction Interface provides uniform access to services of underl'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Memory Interface header file * * \details The Memory Abstraction Interface provides uniform access to services of underlying * Memory Hardware abstraction (MemHwA) modules, i.e. EEPROM Abstraction (EA) and * Flash EEPROM Emulation (FEE). Th

*Repository path:* `MemIf/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MemIf.c` |
| `include/` (2 header(s)) | `MemIf.h`, `MemIf_Types.h` |
| `autosar/` (2 ARXML) | `MemIf_SafeBSW_pre.arxml`, `MemIf_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `MemIf_Read`
- `MemIf_Write`
- `MemIf_InvalidateBlock`
- `MemIf_EraseImmediateBlock`
- `MemIf_Cancel`
- `MemIf_GetStatus`
- `MemIf_GetJobResult`
- `MemIf_SetMode`
- `MemIf_DetChkDeviceIndex`
- `MemIf_IsBitSet`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Std_Types.h`
- `MemIf.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_MemIf](../memif__technicalreference-memif-pdf/)

Source files remain in the repository next to this documentation.

