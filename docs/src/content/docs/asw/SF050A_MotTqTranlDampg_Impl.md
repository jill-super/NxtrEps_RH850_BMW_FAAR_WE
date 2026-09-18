---
title: 'SF050A MotTqTranlDampg'
description: 'SF050A_MotTqTranlDampg_Impl (ASW). Implementation Transitional damping - SF050A.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation Transitional damping - SF050A.

*Repository path:* `SF050A_MotTqTranlDampg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotTqTranlDampg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `SwOpCtrlPart1`
- `SwOpCtrlPart2`
- `MotTqTranlDampgInit1`
- `MotTqTranlDampgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_MotTqTranlDampg.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `SysGlbPrm.h`
- `MotTqTranlDampg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotTqTranlDampg_IntegrationManual](../sf050a_mottqtranldampg_impl__mottqtranldampg-integrationmanual-doc/)
- [MotTqTranlDampg_MDD](../sf050a_mottqtranldampg_impl__mottqtranldampg-mdd-docx/)

Source files remain in the repository next to this documentation.

