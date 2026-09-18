---
title: 'ES220A HwTq4Meas'
description: 'ES220A_HwTq4Meas_Impl (CDD). Adc Diagnostic Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Adc Diagnostic Complex Driver Header

*Repository path:* `ES220A_HwTq4Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 12 file(s), nexteer: 18 file(s), vector: 11 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_HwTq4Meas.c`, `CDD_HwTq4Meas_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_HwTq4Meas.h`, `CDD_HwTq4Meas_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 13):

- `HwTq4MeasPer1`
- `HwTqQlfr`
- `HwTq4AutTrim_Oper`
- `HwTq4ClrSnsrSca_Oper`
- `HwTq4ClrTrim_Oper`
- `HwTq4MeasInit1`
- `HwTq4MeasPer2`
- `HwTq4MeasPer3`
- `HwTq4MeasPer4`
- `HwTq4ReadSnsrSca_Oper`
- `HwTq4ReadTrim_Oper`
- `HwTq4SnsrScaPrfmdSts_Oper`
- `HwTq4TrimPrfmdSts_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_CDD_HwTq4Meas.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `CDD_HwTq4Meas_Cfg.h`
- `CDD_HwTq4Meas_MemMap.h`
- `CDD_HwTq4Meas.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_HwTq4Meas_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HwTq4Meas_IntegrationManual](../es220a_hwtq4meas_impl__hwtq4meas-integrationmanual-doc/)
- [HwTq4Meas_MDD](../es220a_hwtq4meas_impl__hwtq4meas-mdd-docx/)

Source files remain in the repository next to this documentation.

