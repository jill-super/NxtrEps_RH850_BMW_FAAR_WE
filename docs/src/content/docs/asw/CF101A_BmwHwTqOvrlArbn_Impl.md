---
title: 'CF101A BmwHwTqOvrlArbn'
description: 'CF101A_BmwHwTqOvrlArbn_Impl (ASW). CF101A Implementation - BMW Handwheel Torque Overlay Arbitration'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CF101A Implementation - BMW Handwheel Torque Overlay Arbitration

*Repository path:* `CF101A_BmwHwTqOvrlArbn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwHwTqOvrlArbn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `FctlErr`
- `HwTqOvrlArbn`
- `BmwHwTqOvrlArbnInit1`
- `BmwHwTqOvrlArbnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_BmwHwTqOvrlArbn.h`
- `ArchGlbPrm.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `BmwHwTqOvrlArbn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwHwTqOvrlArbn_IntegrationManual](../cf101a_bmwhwtqovrlarbn_impl__bmwhwtqovrlarbn-integrationmanual-doc/)
- [BmwHwTqOvrlArbn_MDD](../cf101a_bmwhwtqovrlarbn_impl__bmwhwtqovrlarbn-mdd-docx/)

Source files remain in the repository next to this documentation.

