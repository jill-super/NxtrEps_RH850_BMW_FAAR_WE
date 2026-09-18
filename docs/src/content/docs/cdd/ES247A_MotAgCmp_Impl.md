---
title: 'ES247A MotAgCmp'
description: 'ES247A_MotAgCmp_Impl (CDD). Motor Angle Compensation Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Motor Angle Compensation Header

*Repository path:* `ES247A_MotAgCmp_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 14 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_MotAgCmp.c`, `CDD_MotAgCmp_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_MotAgCmp.h`, `CDD_MotAgCmp_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `MotAgCmpPer1`
- `MotAgCmpBackEmfRead_Oper`
- `MotAgCmpBackEmfWr_Oper`
- `MotAgCmpInit1`
- `MotAgCmpPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_CDD_MotAgCmp.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `CDD_MotAgCmp_MemMap.h`
- `CDD_MotAgCmp.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotAgCmp_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAgCmp_IntegrationManual](../es247a_motagcmp_impl__motagcmp-integrationmanual-doc/)
- [MotAgCmp_MDD](../es247a_motagcmp_impl__motagcmp-mdd-doc/)

Source files remain in the repository next to this documentation.

