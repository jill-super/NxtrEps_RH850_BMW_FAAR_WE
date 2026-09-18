---
title: 'ES208A CurrMeasArbn'
description: 'ES208A_CurrMeasArbn_Impl (CDD). Current Measurement Arbitration Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Current Measurement Arbitration Complex Driver Header

*Repository path:* `ES208A_CurrMeasArbn_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_CurrMeasArbn.c`, `CDD_CurrMeasArbn_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_CurrMeasArbn.h`, `CDD_CurrMeasArbn_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `CurrMeasArbnPer1`
- `CurrMeasArbnInit1`
- `SigAvlCheck`
- `ParkTransformation`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_CurrMeasArbn.h`
- `CDD_CurrMeasArbn_MemMap.h`
- `CDD_CurrMeasArbn.h`
- `CDD_MotCtrlMgr_Data.h`
- `NxtrMath.h`
- `CDD_CurrMeasArbn_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CurrMeasArbn_IntegrationManual](../es208a_currmeasarbn_impl__currmeasarbn-integrationmanual-docx/)
- [CurrMeasArbn_MDD](../es208a_currmeasarbn_impl__currmeasarbn-mdd-doc/)

Source files remain in the repository next to this documentation.

