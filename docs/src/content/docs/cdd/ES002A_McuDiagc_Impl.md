---
title: 'ES002A McuDiagc'
description: 'ES002A_McuDiagc_Impl (CDD). MCU Diagnostics Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

MCU Diagnostics Complex Driver Header

*Repository path:* `ES002A_McuDiagc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 15 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_McuDiagc.c`, `CDD_McuDiagc_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_McuDiagc.h`, `CDD_McuDiagc_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `McuDiagcPer1`
- `McuDiagcInit1`
- `McuDiagcPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_CDD_McuDiagc.h`
- `NxtrMath.h`
- `McuErrInj.h`
- `CDD_McuDiagc_MemMap.h`
- `CDD_McuDiagc.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_McuDiagc_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [McuDiagc_IntegrationManual](../es002a_mcudiagc_impl__mcudiagc-integrationmanual-docx/)
- [McuDiagc_MDD](../es002a_mcudiagc_impl__mcudiagc-mdd-doc/)

Source files remain in the repository next to this documentation.

