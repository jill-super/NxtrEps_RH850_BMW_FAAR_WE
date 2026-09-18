---
title: 'CF069A BmwStReqMgr'
description: 'CF069A_BmwStReqMgr_Impl (ASW). Implementation of BMW State Request Manager'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW State Request Manager

*Repository path:* `CF069A_BmwStReqMgr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwStReqMgr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 8):

- `Override`
- `CalcOfStsSteerAssiAndEpsFctSts`
- `StsDrvrActvyTmr`
- `AssiOnToOffFlg`
- `AllwToOff`
- `TargetECUState`
- `BmwStReqMgrInit1`
- `BmwStReqMgrPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwStReqMgr.h`
- `NxtrMath.h`
- `BmwStReqMgr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwStReqMgr_IntegrationManual](../cf069a_bmwstreqmgr_impl__bmwstreqmgr-integrationmanual-doc/)
- [BmwStReqMgr_MDD](../cf069a_bmwstreqmgr_impl__bmwstreqmgr-mdd-docx/)

Source files remain in the repository next to this documentation.

