---
title: 'CM620B MotAg0Meas'
description: 'CM620B_MotAg0Meas_Impl (CDD). CSIH1 peripheral configuration and motor Angle 0 measurement Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CSIH1 peripheral configuration and motor Angle 0 measurement Complex Driver Header

*Repository path:* `CM620B_MotAg0Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 19 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_MotAg0Meas.c`, `CDD_MotAg0Meas_MotCtrl.c` |
| `include/` (3 header(s)) | `CDD_MotAg0Meas.h`, `CDD_MotAg0Meas_MotCtrl_MemMap.h`, `CDD_MotAg0Meas_private.h` |
| `autosar/` (4 ARXML) | `CDD_MotAg0Meas_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `MotAg0MeasPer1`
- `MotAg0CfgLoPwrMod`
- `ProcessErrorRegAndDieRevCtr`
- `SPIvsENCA`
- `MotAgFaultProcessing`
- `CalcNtcPrm`
- `SetMotAg0FltNtc`
- `CalculateMotAgTurnCntr`
- `CalcCorrnTbl`
- `MotAg0CoeffTblRead_Oper`
- `MotAg0CoeffTblWr_Oper`
- `MotAg0MeasInit1`
- `MotAg0MeasPer2`
- `MotAg0MeasPer3`
- `SPI_AngleRawProcess`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 14):

- `Rte_CDD_MotAg0Meas.h`
- `csih_regs.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `CDD_MotAg0Meas.h`
- `CDD_MotAg0Meas_private.h`
- `CDD_MotAg0Meas_Cfg.h`
- `CDD_MotAg0Meas_MemMap.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotAg3Meas.h`
- `CDD_NxtrTi.h`
- `FltInj.h`
- `CDD_MotAg0Meas_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAg0Meas_IntegrationManual](../cm620b_motag0meas_impl__motag0meas-integrationmanual-doc/)
- [MotAg0Meas_MDD](../cm620b_motag0meas_impl__motag0meas-mdd-docx/)

Source files remain in the repository next to this documentation.

