---
title: 'CF080A BmwVehSpd'
description: 'CF080A_BmwVehSpd_Impl (ASW). Implementation of BMW Vehicle Speed - CF080A FDD'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW Vehicle Speed - CF080A FDD

*Repository path:* `CF080A_BmwVehSpd_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwVehSpd.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `Cntr`
- `VehSpdVldCalcn`
- `VehSpdRateLim`
- `ProcessSecondAndGateState`
- `ProcessThirdAndGateState`
- `ProcessSixthAndGateState`
- `ProcessFourthAndGateState`
- `ProcessThridConditionOfOrGate`
- `BmwVehSpdInit1`
- `BmwVehSpdPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BmwVehSpd.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `BmwVehSpd_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwVehSpd_IntegrationManual](../cf080a_bmwvehspd_impl__bmwvehspd-integrationmanual-doc/)
- [BmwVehSpd_MDD](../cf080a_bmwvehspd_impl__bmwvehspd-mdd-docx/)

Source files remain in the repository next to this documentation.

