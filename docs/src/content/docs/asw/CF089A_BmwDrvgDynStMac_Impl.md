---
title: 'CF089A BmwDrvgDynStMac'
description: 'CF089A_BmwDrvgDynStMac_Impl (ASW). CF089A Implementation - BMW Driving Dynamics State Machine'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CF089A Implementation - BMW Driving Dynamics State Machine

*Repository path:* `CF089A_BmwDrvgDynStMac_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwDrvgDynStMac.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 14):

- `DetermineErrorMode`
- `Fac`
- `AssiLvlCnd`
- `CheckActivityTime`
- `CheckDeactivateTime`
- `ErrorIfTi`
- `StateMachine`
- `StateMachineInit`
- `StateMachineIfAvl`
- `StateMachineIfActv`
- `StateMachineStbEpsSts`
- `StateMachineEntry`
- `BmwDrvgDynStMacInit1`
- `BmwDrvgDynStMacPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BmwDrvgDynStMac.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `BmwDrvgDynStMac_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwDrvgDynStMac_IntegrationManual](../cf089a_bmwdrvgdynstmac_impl__bmwdrvgdynstmac-integrationmanual-doc/)
- [BmwDrvgDynStMac_MDD](../cf089a_bmwdrvgdynstmac_impl__bmwdrvgdynstmac-mdd-docx/)

Source files remain in the repository next to this documentation.

