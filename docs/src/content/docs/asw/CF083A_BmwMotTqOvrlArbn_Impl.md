---
title: 'CF083A BmwMotTqOvrlArbn'
description: 'CF083A_BmwMotTqOvrlArbn_Impl (ASW). Implementation of CF083A - BmwMotTqOvrlArbn'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of CF083A - BmwMotTqOvrlArbn

*Repository path:* `CF083A_BmwMotTqOvrlArbn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMotTqOvrlArbn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `ChkForFctlErr`
- `BmwMotTqOvrlArbnInit1`
- `BmwMotTqOvrlArbnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_BmwMotTqOvrlArbn.h`
- `Dcm.h`
- `NxtrMath.h`
- `SysGlbPrm.h`
- `BmwMotTqOvrlArbn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwMotTqOvrlArbn_IntegrationManual](../cf083a_bmwmottqovrlarbn_impl__bmwmottqovrlarbn-integrationmanual-doc/)
- [BmwMotTqOvrlArbn_MDD](../cf083a_bmwmottqovrlarbn_impl__bmwmottqovrlarbn-mdd-docx/)

Source files remain in the repository next to this documentation.

