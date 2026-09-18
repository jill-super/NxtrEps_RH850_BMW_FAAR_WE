---
title: 'SF040A MotVel'
description: 'SF040A_MotVel_Impl (ASW). Motor velocity Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Motor velocity Complex Driver Header

*Repository path:* `SF040A_MotVel_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 15 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_MotVel.c`, `CDD_MotVel_MotCtrl.c` |
| `include/` (3 header(s)) | `CDD_MotVel.h`, `CDD_MotVel_MotCtrl_MemMap.h`, `CDD_MotVel_private.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `MotVelPer1`
- `MotVelInit1`
- `MotVelPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_CDD_MotVel.h`
- `CDD_MotVel_private.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `CDD_MotVel_MemMap.h`
- `CDD_MotVel.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotVel_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotVel_Integration Manual](../sf040a_motvel_impl__motvel-integration-manual-docx/)
- [MotVel_MDD](../sf040a_motvel_impl__motvel-mdd-docx/)

Source files remain in the repository next to this documentation.

