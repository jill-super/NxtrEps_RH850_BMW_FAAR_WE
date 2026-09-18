---
title: 'NM100A MotVelCtrl'
description: 'NM100A_MotVelCtrl_Impl (ASW). Implementation of Motor Velocity Control FDD NM100A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Motor Velocity Control FDD NM100A

*Repository path:* `NM100A_MotVelCtrl_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotVelCtrl.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `FPIDControl`
- `GetCtrlPrm_Oper`
- `MotVelCtrlInit1`
- `MotVelCtrlPer1`
- `SetCtrlPrm_Oper`
- `StopCtrl_Oper`
- `StrtCtrl_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_MotVelCtrl.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `MotVelCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotVelCtrl_IntegrationManual](../nm100a_motvelctrl_impl__motvelctrl-integrationmanual-doc/)
- [MotVelCtrl_MDD](../nm100a_motvelctrl_impl__motvelctrl-mdd-docx/)

Source files remain in the repository next to this documentation.

