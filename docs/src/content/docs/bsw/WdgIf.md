---
title: 'WdgIf WdgIf'
description: 'WdgIf (BSW). WdgIf header file * * \details This is the header file of the module WdgIf'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

WdgIf header file * * \details This is the header file of the module WdgIf

*Repository path:* `WdgIf/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 4 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `WdgIf.c` |
| `include/` (3 header(s)) | `WdgIf.h`, `WdgIf_Cfg.h`, `WdgIf_Types.h` |
| `autosar/` (1 ARXML) | `WdgIf_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `WdgIf_SetMode`
- `WdgIf_SetTriggerCondition`
- `WdgIf_SetTriggerWindow`
- `WdgIf_GetVersionInfo`
- `wdgif_statecombiner_check_slave_timing`
- `wdgif_statecombiner_setmode`
- `wdgif_statecombiner_settriggerwindow`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `WdgIf.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_WdgIf](../wdgif__technicalreference-wdgif-pdf/)

Source files remain in the repository next to this documentation.

