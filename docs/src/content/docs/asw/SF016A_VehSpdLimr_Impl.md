---
title: 'SF016A VehSpdLimr'
description: 'SF016A_VehSpdLimr_Impl (ASW). Implements the SF016A_VehSpdLimr_Design FDD.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implements the SF016A_VehSpdLimr_Design FDD.

*Repository path:* `SF016A_VehSpdLimr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `VehSpdLimr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `VehSpdLimrPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_VehSpdLimr.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `SysGlbPrm.h`
- `VehSpdLimr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [VehSpdLimr_IntegrationManual](../sf016a_vehspdlimr_impl__vehspdlimr-integrationmanual-doc/)
- [VehSpdLimr_MDD](../sf016a_vehspdlimr_impl__vehspdlimr-mdd-docx/)

Source files remain in the repository next to this documentation.

