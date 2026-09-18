---
title: 'ES221A HwTq5Meas'
description: 'ES221A_HwTq5Meas_Impl (CDD). Adc Diagnostic Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Adc Diagnostic Complex Driver Header

*Repository path:* `ES221A_HwTq5Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 12 file(s), nexteer: 18 file(s), vector: 11 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_HwTq5Meas.c`, `CDD_HwTq5Meas_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_HwTq5Meas.h`, `CDD_HwTq5Meas_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 13):

- `HwTq5MeasPer1`
- `HwTqQlfr`
- `HwTq5AutTrim_Oper`
- `HwTq5ClrSnsrSca_Oper`
- `HwTq5ClrTrim_Oper`
- `HwTq5MeasInit1`
- `HwTq5MeasPer2`
- `HwTq5MeasPer3`
- `HwTq5MeasPer4`
- `HwTq5ReadSnsrSca_Oper`
- `HwTq5ReadTrim_Oper`
- `HwTq5SnsrScaPrfmdSts_Oper`
- `HwTq5TrimPrfmdSts_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_CDD_HwTq5Meas.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `CDD_HwTq5Meas_Cfg.h`
- `CDD_HwTq5Meas_MemMap.h`
- `CDD_HwTq5Meas.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_HwTq5Meas_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HwTq5Meas_IntegrationManual](../es221a_hwtq5meas_impl__hwtq5meas-integrationmanual-doc/)
- [HwTq5Meas_MDD](../es221a_hwtq5meas_impl__hwtq5meas-mdd-docx/)

Source files remain in the repository next to this documentation.

