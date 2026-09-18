---
title: 'Det Det'
description: 'Det (BSW). Header of Default Error Tracer * * \details Contains definitions, types, externals and prototype declarations. * \trace'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

Header of Default Error Tracer * * \details Contains definitions, types, externals and prototype declarations. * \trace SPEC-2880976, SPEC-2880977

*Repository path:* `Det/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 2 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Det.c` |
| `include/` (1 header(s)) | `Det.h` |
| `autosar/` (2 ARXML) | `Det_bswmd.arxml`, `Det_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 11):

- `Det_Init`
- `Det_Start`
- `Det_InitMemory`
- `Det_ReportError`
- `Det_ReportRuntimeError`
- `Det_ReportTransientFault`
- `Det_GetVersionInfo`
- `Det_CheckFilterMatch`
- `Det_LogError`
- `Det_CanoeOutput`
- `Det_EndlessLoop`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Det.h`
- `Compiler.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Det](../det__technicalreference-det-pdf/)

Source files remain in the repository next to this documentation.

