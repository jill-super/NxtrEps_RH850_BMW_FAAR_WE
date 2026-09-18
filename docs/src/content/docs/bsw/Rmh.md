---
title: 'Rmh Rmh'
description: 'Rmh (BSW). BMW Remote Measurement Handler (BAC measurement services).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW Remote Measurement Handler (BAC measurement services).

*Repository path:* `Rmh/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 6 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `RmhClassic.c`, `RmhClassic_Cdd.c`, `RmhClassic_Int.c` |
| `include/` (3 header(s)) | `RmhClassic.h`, `RmhClassic_Cdd.h`, `RmhClassic_Int.h` |
| `autosar/` (1 ARXML) | `RmhClassic_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `Rmh_FindMapping`
- `Rmh_RxRequestMsg`
- `Rmh_TriggerComIPDUSend`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `RmhClassic_Version.h`
- `RmhClassic.h`
- `RmhClassic_Int.h`
- `RmhClassic_MemMap.h`
- `RmhClassic_Cfg.h`
- `RmhClassic_Cdd.h`
- `Com.h`
- `RmhClassic_Cdd_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [RmhClassic_IntegrationManual](../rmh__rmhclassic-integrationmanual-pdf/)
- [RmhClassic_ReleaseNotes](../rmh__rmhclassic-releasenotes-pdf/)

Source files remain in the repository next to this documentation.

