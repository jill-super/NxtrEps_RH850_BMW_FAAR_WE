---
title: 'SF102A MotCtrlPrmEstimn'
description: 'SF102A_MotCtrlPrmEstimn_Impl (ASW). Implementation of "Motor Control Parameter Estimation" component'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of "Motor Control Parameter Estimation" component

*Repository path:* `SF102A_MotCtrlPrmEstimn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotCtrlPrmEstimn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `GetMotPrmNomEol_Oper`
- `MotCtrlPrmEstimnInit1`
- `MotCtrlPrmEstimnPer1`
- `MotCtrlPrmEstimnPer2`
- `SetMotPrmNomEol_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_MotCtrlPrmEstimn.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `MotCtrlPrmEstimn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotCtrlPrmEstimn_IntegrationManual](../sf102a_motctrlprmestimn_impl__motctrlprmestimn-integrationmanual-doc/)
- [MotCtrlPrmEstimn_MDD](../sf102a_motctrlprmestimn_impl__motctrlprmestimn-mdd-docx/)

Source files remain in the repository next to this documentation.

