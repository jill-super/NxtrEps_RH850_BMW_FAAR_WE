---
title: 'CF040A BmwTqOvrlCdngAndDrvgDynFac'
description: 'CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl (ASW). The BMW Output Torque Overlay Command functionality and conditioning of the BMW Driving Dynamic Factors'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

The BMW Output Torque Overlay Command functionality and conditioning of the BMW Driving Dynamic Factors

*Repository path:* `CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 14 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwTqOvrlCdngAndDrvgDynFac.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 9):

- `TqOvrlCdng`
- `StTranDetn`
- `CalcCdndTqOvrl`
- `CalcnLimdCdndTqOvrl`
- `CalcnEffortCmdSca`
- `CalcnDampgCmdSca`
- `CalcnRtnCmdSca`
- `BmwTqOvrlCdngAndDrvgDynFacInit1`
- `BmwTqOvrlCdngAndDrvgDynFacPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_BmwTqOvrlCdngAndDrvgDynFac.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `FltInj.h`
- `BmwTqOvrlCdngAndDrvgDynFac_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwTqOvrlCdngAndDrvgDynFac_IntegrationManual](../cf040a_bmwtqovrlcdnganddrvgdynfac_impl__bmwtqovrlcdnganddrvgdynfac-integrationmanual-doc/)
- [BmwTqOvrlCdngAndDrvgDynFac_MDD](../cf040a_bmwtqovrlcdnganddrvgdynfac_impl__bmwtqovrlcdnganddrvgdynfac-mdd-docx/)

Source files remain in the repository next to this documentation.

