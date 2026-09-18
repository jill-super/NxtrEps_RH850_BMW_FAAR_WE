---
title: 'SF019D PwrLimr'
description: 'SF019D_PwrLimr_Impl (ASW). Implementation of Power Limiter - Current Mode -- SF019D'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Power Limiter - Current Mode -- SF019D

*Repository path:* `SF019D_PwrLimr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 13 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PwrLimr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `AssiLimCdn`
- `PwrLimrInit1`
- `PwrLimrPer1`
- `PwrLimrPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_PwrLimr.h`
- `ArchGlbPrm.h`
- `ElecGlbPrm.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `SysGlbPrm.h`
- `PwrLimr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PwrLimr_IntegrationManual](../sf019d_pwrlimr_impl__pwrlimr-integrationmanual-doc/)
- [PwrLimr_MDD](../sf019d_pwrlimr_impl__pwrlimr-mdd-docx/)

Source files remain in the repository next to this documentation.

