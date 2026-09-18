---
title: 'SF006A TEstimn'
description: 'SF006A_TEstimn_Impl (ASW). Implementation of Temperature Estimation FDD SF006A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Temperature Estimation FDD SF006A

*Repository path:* `SF006A_TEstimn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 13 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `TEstimn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `FltMtgtnCalSeln`
- `TEstimnInit1`
- `TEstimnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_TEstimn.h`
- `NxtrMath.h`
- `NxtrFil.h`
- `ArchGlbPrm.h`
- `TEstimn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TEstimn_IntegrationManual](../sf006a_testimn_impl__testimn-integrationmanual-doc/)
- [TEstimn_MDD](../sf006a_testimn_impl__testimn-mdd-docx/)

Source files remain in the repository next to this documentation.

