---
title: 'SF112A SteerCmdArbnAndLim'
description: 'SF112A_SteerCmdArbnAndLim_Impl (ASW). Steer Command Arbitration And Limit arbitrates between different sources of Motor Torque Command'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Steer Command Arbitration And Limit arbitrates between different sources of Motor Torque Command

*Repository path:* `SF112A_SteerCmdArbnAndLim_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `SteerCmdArbnAndLim.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `SteerCmdArbnAndLimStMac`
- `TranDeb`
- `SetNtcs`
- `SetManTqCmd_Oper`
- `SteerCmdArbnAndLimInit1`
- `SteerCmdArbnAndLimPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_SteerCmdArbnAndLim.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `SteerCmdArbnAndLim_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [SteerCmdArbnAndLim_IntegrationManual](../sf112a_steercmdarbnandlim_impl__steercmdarbnandlim-integrationmanual-doc/)
- [SteerCmdArbnAndLim_MDD](../sf112a_steercmdarbnandlim_impl__steercmdarbnandlim-mdd-docx/)

Source files remain in the repository next to this documentation.

