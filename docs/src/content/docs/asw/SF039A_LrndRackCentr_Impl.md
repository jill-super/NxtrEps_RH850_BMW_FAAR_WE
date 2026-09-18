---
title: 'SF039A LrndRackCentr'
description: 'SF039A_LrndRackCentr_Impl (ASW). Implementation of Learned Rack Center FDD (SF039A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Learned Rack Center FDD (SF039A)

*Repository path:* `SF039A_LrndRackCentr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `LrndRackCentr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `ManLrnRackCentr`
- `ChkRackCentr`
- `LrndRackCentrInit1`
- `LrndRackCentrPer1`
- `RstRackCentrMotAg_Oper`
- `RstRackCentrMotRev_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_LrndRackCentr.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `NxtrFil.h`
- `LrndRackCentr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [LrndRackCentr_IntegrationManual](../sf039a_lrndrackcentr_impl__lrndrackcentr-integrationmanual-doc/)
- [LrndRackCentr_MDD](../sf039a_lrndrackcentr_impl__lrndrackcentr-mdd-docx/)

Source files remain in the repository next to this documentation.

