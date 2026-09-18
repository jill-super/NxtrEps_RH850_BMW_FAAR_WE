---
title: 'ES259B BattVltgCorrln'
description: 'ES259B_BattVltgCorrln_Impl (CDD). Implementation of Battery Voltage Correlation FDD ES259B'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Battery Voltage Correlation FDD ES259B

*Repository path:* `ES259B_BattVltgCorrln_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BattVltgCorrln.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `RngChk`
- `DetInstCorrln`
- `DetIdptSig`
- `DetCorrlnSts`
- `BattVltgDiag`
- `BattVltgCorrlnInit1`
- `BattVltgCorrlnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BattVltgCorrln.h`
- `ElecGlbPrm.h`
- `NxtrMath.h`
- `BattVltgCorrln_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BattVltgCorrln_IntegrationManual](../es259b_battvltgcorrln_impl__battvltgcorrln-integrationmanual-doc/)
- [BattVltgCorrln_MDD](../es259b_battvltgcorrln_impl__battvltgcorrln-mdd-doc/)

Source files remain in the repository next to this documentation.

