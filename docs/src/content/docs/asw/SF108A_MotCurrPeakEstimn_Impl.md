---
title: 'SF108A MotCurrPeakEstimn'
description: 'SF108A_MotCurrPeakEstimn_Impl (ASW). Implementation of MotCurrPeakEstimn FDD SF108A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of MotCurrPeakEstimn FDD SF108A

*Repository path:* `SF108A_MotCurrPeakEstimn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotCurrPeakEstimn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `MotCurrPeakEstimnInit1`
- `MotCurrPeakEstimnPer1`
- `MotCurrPeakEstimnPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_MotCurrPeakEstimn.h`
- `NxtrFil.h`
- `ArchGlbPrm.h`
- `MotCurrPeakEstimn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotCurrPeakEstimn_IntegrationManual](../sf108a_motcurrpeakestimn_impl__motcurrpeakestimn-integrationmanual-doc/)
- [MotCurrPeakEstimn_MDD](../sf108a_motcurrpeakestimn_impl__motcurrpeakestimn-mdd-docx/)

Source files remain in the repository next to this documentation.

