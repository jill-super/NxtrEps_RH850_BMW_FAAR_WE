---
title: 'SF013A PullCmpActv'
description: 'SF013A_PullCmpActv_Impl (ASW). Implementation of Active Pull Compensation SF013A.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Active Pull Compensation SF013A.

*Repository path:* `SF013A_PullCmpActv_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PullCmpActv.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `ActvCmpEna`
- `CalcIntgtrGain`
- `ErrIntgtrActvLim`
- `GetPullCmpPrm_Oper`
- `PullCmpActvInit1`
- `PullCmpActvPer1`
- `PullCmpActvPer2`
- `RstPullCmp_Oper`
- `SetPullCmpLongTerm_Oper`
- `SetPullCmpShoTerm_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_PullCmpActv.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `ArchGlbPrm.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `FltInj.h`
- `PullCmpActv_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PullCmpActv_IntegrationManual](../sf013a_pullcmpactv_impl__pullcmpactv-integrationmanual-doc/)
- [PullCmpActv_MDD](../sf013a_pullcmpactv_impl__pullcmpactv-mdd-docx/)

Source files remain in the repository next to this documentation.

