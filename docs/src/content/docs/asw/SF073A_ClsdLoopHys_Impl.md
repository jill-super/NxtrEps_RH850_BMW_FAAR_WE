---
title: 'SF073A ClsdLoopHys'
description: 'SF073A_ClsdLoopHys_Impl (ASW). Closed Loop Hysteresis provides a controllable hysteresis shaped torque based on a rack load'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Closed Loop Hysteresis provides a controllable hysteresis shaped torque based on a rack load

*Repository path:* `SF073A_ClsdLoopHys_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `ClsdLoopHys.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `Interpolate`
- `IntgtrLimCalcn`
- `CompCalcn1`
- `CompCalcn2`
- `SysFricOffsLimdCalc`
- `ClsdLoopHysInit1`
- `ClsdLoopHysPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_ClsdLoopHys.h`
- `NxtrMath.h`
- `NxtrFixdpt.h`
- `NxtrIntrpn.h`
- `ArchGlbPrm.h`
- `ClsdLoopHys_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ClsdLoopHys_IntegrationManual](../sf073a_clsdloophys_impl__clsdloophys-integrationmanual-doc/)
- [ClsdLoopHys_MDD](../sf073a_clsdloophys_impl__clsdloophys-mdd-docx/)

Source files remain in the repository next to this documentation.

