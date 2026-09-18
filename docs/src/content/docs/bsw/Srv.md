---
title: 'Srv Srv'
description: 'Srv (BSW). BMW BAC services library (bootmode helpers and shared utilities).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW BAC services library (bootmode helpers and shared utilities).

*Repository path:* `Srv/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Srv_BootMode.c` |
| `include/` (2 header(s)) | `Srv_BluSweCheckSum.h`, `Srv_BootMode.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `Srv_BootModeInit`
- `Srv_BootDcmStatusGet`
- `Srv_BootModeGet`
- `Srv_BootModeSet`
- `Srv_ParallelFlashModeGet`
- `Srv_ParallelFlashModeSet`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Srv_BootMode.h`
- `Srv_Cfg.h`
- `Srv_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [IntegrationManual_Srv](../srv__integrationmanual-srv-pdf/)
- [ReleaseNotes_Srv](../srv__releasenotes-srv-pdf/)

Source files remain in the repository next to this documentation.

