---
title: 'CM640B MotAg1Meas'
description: 'CM640B_MotAg1Meas_Impl (CDD). CSIH3 peripheral configuration and motor Angle 1 measurement Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CSIH3 peripheral configuration and motor Angle 1 measurement Complex Driver Header

*Repository path:* `CM640B_MotAg1Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 19 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_MotAg1Meas.c`, `CDD_MotAg1Meas_MotCtrl.c` |
| `include/` (3 header(s)) | `CDD_MotAg1Meas.h`, `CDD_MotAg1Meas_MotCtrl_MemMap.h`, `CDD_MotAg1Meas_private.h` |
| `autosar/` (4 ARXML) | `CDD_MotAg1Meas_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `MotAg1MeasPer1`
- `MotAg1CfgLoPwrMod`
- `ProcessErrorRegAndDieRevCtr`
- `SPIvsENCA`
- `MotAgFaultProcessing`
- `CalcNtcPrm`
- `SetMotAg1FltNtc`
- `CalculateMotAgTurnCntr`
- `CalcCorrnTbl`
- `MotAg1CoeffTblRead_Oper`
- `MotAg1CoeffTblWr_Oper`
- `MotAg1MeasInit1`
- `MotAg1MeasPer2`
- `SPI_AngleRawProcess`
- `CompensateMechMtrPos`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Rte_CDD_MotAg1Meas.h`
- `csih_regs.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `CDD_MotAg1Meas.h`
- `CDD_MotAg1Meas_private.h`
- `CDD_MotAg1Meas_Cfg.h`
- `CDD_MotAg1Meas_MemMap.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotAg4Meas.h`
- `CDD_NxtrTi.h`
- `CDD_MotAg1Meas_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAg1Meas_IntegrationManual](../cm640b_motag1meas_impl__motag1meas-integrationmanual-doc/)
- [MotAg1Meas_MDD](../cm640b_motag1meas_impl__motag1meas-mdd-docx/)

Source files remain in the repository next to this documentation.

