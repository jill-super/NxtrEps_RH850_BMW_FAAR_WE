---
title: 'CF082A BmwPwrPrkgDampg'
description: 'CF082A_BmwPwrPrkgDampg_Impl (ASW). Implementation of CF082A - BMW Power Parking Damping'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of CF082A - BMW Power Parking Damping

*Repository path:* `CF082A_BmwPwrPrkgDampg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwPwrPrkgDampg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BmwPwrPrkgDampgInit1`
- `BmwPwrPrkgDampgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_BmwPwrPrkgDampg.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `BmwPwrPrkgDampg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwPwrPrkgDampg_IntegrationManual](../cf082a_bmwpwrprkgdampg_impl__bmwpwrprkgdampg-integrationmanual-doc/)
- [BmwPwrPrkgDampg_MDD](../cf082a_bmwpwrprkgdampg_impl__bmwpwrprkgdampg-mdd-docx/)

Source files remain in the repository next to this documentation.

