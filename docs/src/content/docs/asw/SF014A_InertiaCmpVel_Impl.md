---
title: 'SF014A InertiaCmpVel'
description: 'SF014A_InertiaCmpVel_Impl (ASW). Implementation of InertiaCmpVel FDD SF014A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of InertiaCmpVel FDD SF014A

*Repository path:* `SF014A_InertiaCmpVel_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `InertiaCmpVel.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `DrvrVelCalc`
- `ADDCoeffCalc`
- `FilCoeffCalc`
- `GenFddIcCmd`
- `DecelGain`
- `NotchCmp`
- `FilNotchInit`
- `FilNotchFullUpdOutp_f32`
- `InertiaCmpVelInit1`
- `InertiaCmpVelPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_InertiaCmpVel.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `FltInj.h`
- `NxtrFil.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `InertiaCmpVel_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [InertiaCmpVel_IntegrationManual](../sf014a_inertiacmpvel_impl__inertiacmpvel-integrationmanual-docx/)
- [InertiaCmpVel_MDD](../sf014a_inertiacmpvel_impl__inertiacmpvel-mdd-docx/)

Source files remain in the repository next to this documentation.

