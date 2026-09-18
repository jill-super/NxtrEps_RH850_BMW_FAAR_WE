---
title: 'IoHwAb IoHwAb'
description: 'IoHwAb (BSW). Mapping to the Det_ReportError() service'
---

:::tip[Origin: Vector-provided · MICROSAR]
Project-configured/generated for this ECU (DaVinci/MICROSAR tooling).
:::

## Purpose

Mapping to the Det_ReportError() service

*Repository path:* `IoHwAb/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 1 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (0 C file(s)) | — |
| `include/` (1 header(s)) | `IoHwAb.h` |
| `autosar/` (1 ARXML) | `IoHwAb_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `IoHwAb_GetVersionInfo`
- `IoHwAb_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

No quoted `#include "..."` dependencies were found in the scanned sources.

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_IoHwAb](../iohwab__technicalreference-iohwab-pdf/)

Source files remain in the repository next to this documentation.

