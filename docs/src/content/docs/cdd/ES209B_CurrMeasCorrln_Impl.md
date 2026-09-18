---
title: 'ES209B CurrMeasCorrln'
description: 'ES209B_CurrMeasCorrln_Impl (CDD). Implementation of Current Measurement Correlation -- ES209B'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Current Measurement Correlation -- ES209B

*Repository path:* `ES209B_CurrMeasCorrln_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CurrMeasCorrln.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `SigAvlChk`
- `CurrMeasCorrlnChk`
- `CurrMeasCorrlnInit1`
- `CurrMeasCorrlnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_CurrMeasCorrln.h`
- `NxtrMath.h`
- `FltInj.h`
- `CurrMeasCorrln_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CurrMeasCorrln_IntegrationManual](../es209b_currmeascorrln_impl__currmeascorrln-integrationmanual-docx/)
- [CurrMeasCorrln_MDD](../es209b_currmeascorrln_impl__currmeascorrln-mdd-docx/)

Source files remain in the repository next to this documentation.

