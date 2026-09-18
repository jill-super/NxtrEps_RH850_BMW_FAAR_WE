---
title: 'CM475A TSG31CfgAndUse'
description: 'CM475A_TSG31CfgAndUse_Impl (CDD). TSG31 Timer Configuration and Use Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

TSG31 Timer Configuration and Use Complex Driver Header

*Repository path:* `CM475A_TSG31CfgAndUse_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 16 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_TSG31CfgAndUse.c`, `CDD_TSG31CfgAndUse_MotCtrl.c` |
| `include/` (3 header(s)) | `CDD_TSG31CfgAndUse.h`, `CDD_TSG31CfgAndUse_MotCtrl_MemMap.h`, `CDD_TSG31CfgAndUse_private.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 11):

- `TSG31CfgAndUsePer1`
- `CnvNanoSecToTmrCnt`
- `MapPinsToGpio`
- `MapFetCtrlSigToGpioAndSetLow`
- `NoTranSysStNotEn`
- `TranToEn`
- `TranFromEn`
- `NoTranSysStIsEn`
- `TSG31CfgAndUseInit1`
- `TSG31CfgAndUsePer2`
- `MissUpdtCntrDiagc`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_CDD_TSG31CfgAndUse.h`
- `CDD_TSG31CfgAndUse_private.h`
- `ElecGlbPrm.h`
- `tsg3_regs.h`
- `CDD_TSG31CfgAndUse_MemMap.h`
- `CDD_TSG31CfgAndUse.h`
- `CDD_MotCtrlMgr_Data.h`
- `NxtrMath.h`
- `CDD_TSG31CfgAndUse_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TSG31CfgAndUse Integration Manual](../cm475a_tsg31cfganduse_impl__tsg31cfganduse-integration-manual-doc/)
- [TSG31CfgAndUse_MDD](../cm475a_tsg31cfganduse_impl__tsg31cfganduse-mdd-doc/)

Source files remain in the repository next to this documentation.

