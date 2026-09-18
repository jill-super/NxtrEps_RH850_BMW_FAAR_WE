---
title: 'ES249B MotAgCorrln'
description: 'ES249B_MotAgCorrln_Impl (CDD). Implementation of Motor Angle Correlation FDD ES249B'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Motor Angle Correlation FDD ES249B

*Repository path:* `ES249B_MotAgCorrln_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotAgCorrln.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `MotAgSigAvlCheck`
- `MotAgOKCheck`
- `MotAgCorrlnInit1`
- `MotAgCorrlnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_MotAgCorrln.h`
- `NxtrMath.h`
- `FltInj.h`
- `MotAgCorrln_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAgCorrln_Integration Manual](../es249b_motagcorrln_impl__motagcorrln-integration-manual-docx/)
- [MotAgCorrln_MDD](../es249b_motagcorrln_impl__motagcorrln-mdd-docx/)

Source files remain in the repository next to this documentation.

