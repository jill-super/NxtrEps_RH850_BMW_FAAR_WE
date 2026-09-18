---
title: 'DF001A FltInj'
description: 'DF001A_FltInj_Impl (CDD). Fault Injection definitions'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Fault Injection definitions

*Repository path:* `DF001A_FltInj_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `FltInj.c` |
| `include/` (1 header(s)) | `FltInj.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `FltInj_f32_Oper`
- `FltInj_logl_Oper`
- `FltInj_u08_Oper`
- `FltInj_u0p16_Oper`
- `FltInjPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_FltInj.h`
- `FltInj.h`
- `ArchGlbPrm.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `FltInj_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [FltInj_IntegrationManual](../df001a_fltinj_impl__fltinj-integrationmanual-doc/)
- [FltInj_MDD](../df001a_fltinj_impl__fltinj-mdd-docx/)

Source files remain in the repository next to this documentation.

