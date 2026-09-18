---
title: 'CM340A AdcDiagc'
description: 'CM340A_AdcDiagc_Impl (CDD). Implementation of Adc Diagnostics'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Adc Diagnostics

*Repository path:* `CM340A_AdcDiagc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_AdcDiagc.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 12):

- `Adc0StBasdProc`
- `Adc1StBasdProc`
- `AdcDiagcPtrProc`
- `St0Proc`
- `St2Proc`
- `St4Proc`
- `St6Proc`
- `ScanGroupAccrcyChk`
- `SetAdcParFlt`
- `AdcDiagcInit1`
- `AdcDiagcPer1`
- `InjAdcErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_AdcDiagc.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `adcd_regs.h`
- `McuErrInj.h`
- `CDD_AdcDiagc_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [AdcDiagc_IntegrationManual](../cm340a_adcdiagc_impl__adcdiagc-integrationmanual-doc/)
- [AdcDiagc_MDD](../cm340a_adcdiagc_impl__adcdiagc-mdd-docx/)

Source files remain in the repository next to this documentation.

