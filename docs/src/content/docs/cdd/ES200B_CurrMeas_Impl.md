---
title: 'ES200B CurrMeas'
description: 'ES200B_CurrMeas_Impl (CDD). Current Measurement Arbitration Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Current Measurement Arbitration Complex Driver Header

*Repository path:* `ES200B_CurrMeas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 18 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_CurrMeas.c`, `CDD_CurrMeas_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_CurrMeas.h`, `CDD_CurrMeas_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `CurrMeasPer2`
- `OffsetCalibration`
- `GainCalibration`
- `RangeChkWIABC`
- `GainCmdAD`
- `GainCmdBE`
- `GainCmdCF`
- `CmdSafest`
- `OffsCmdHI`
- `OffsCmdLO`
- `OffsCmdZERO`
- `OffsCmdEND`
- `CurrMeasEolGainReq_Oper`
- `CurrMeasEolGainStsReq_Oper`
- `CurrMeasEolOffsReq_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 10):

- `Rte_CDD_CurrMeas.h`
- `CDD_CurrMeas.h`
- `CDD_MotCtrlMgr_Data.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `ArchGlbPrm.h`
- `CDD_CurrMeas_MemMap.h`
- `FltInj.h`
- `NxtrFixdPt.h`
- `CDD_CurrMeas_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CurrMeas_IntegrationManual](../es200b_currmeas_impl__currmeas-integrationmanual-doc/)
- [CurrMeas_MDD](../es200b_currmeas_impl__currmeas-mdd-docx/)

Source files remain in the repository next to this documentation.

