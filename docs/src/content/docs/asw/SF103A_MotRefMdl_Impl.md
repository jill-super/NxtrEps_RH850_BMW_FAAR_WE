---
title: 'SF103A MotRefMdl'
description: 'SF103A_MotRefMdl_Impl (ASW). Current Measurement Arbitration Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Current Measurement Arbitration Complex Driver Header

*Repository path:* `SF103A_MotRefMdl_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 14 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotRefMdl.c` |
| `include/` (1 header(s)) | `MotRefMdl.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 11):

- `PrbcIntrpn`
- `CalcIq`
- `CalcCurrMagSqRef`
- `CurrtoVoltTest`
- `CalcTq`
- `CalcMaxTqPt`
- `CalcMinMotCurr`
- `Decoder`
- `VltgSdlCalc`
- `MotRefMdlInit1`
- `MotRefMdlPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_MotRefMdl.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `ArchGlbPrm.h`
- `NxtrFil.h`
- `MotRefMdl.h`
- `SysGlbPrm.h`
- `MotRefMdl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotRefMdl_IntegrationManual](../sf103a_motrefmdl_impl__motrefmdl-integrationmanual-doc/)
- [MotRefMdl_MDD](../sf103a_motrefmdl_impl__motrefmdl-mdd-doc/)

Source files remain in the repository next to this documentation.

