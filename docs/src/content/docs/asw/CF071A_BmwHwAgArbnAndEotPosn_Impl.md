---
title: 'CF071A BmwHwAgArbnAndEotPosn'
description: 'CF071A_BmwHwAgArbnAndEotPosn_Impl (ASW). Implementation of BMW Handwheel Angle Arbitration And End of Travel Position'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW Handwheel Angle Arbitration And End of Travel Position

*Repository path:* `CF071A_BmwHwAgArbnAndEotPosn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 15 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwHwAgArbnAndEotPosn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `BmwHwAgArbnAndEotPosn_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `HwAgSnsrNotTrimNTC`
- `HwPosnFltDetn`
- `PinionAgFltTmr`
- `OffsCorrnTmr`
- `InitTmr`
- `CalcBmwMotAgOffsSelnSt`
- `CalcBmwMotAgOffsSelnStOffsCmpd`
- `CalcBmwMotAgOffsSelnStSubVal`
- `CalcBmwMotAgOffsSelnStTmpCmpd`
- `CalcBmwMotAgOffsSelnStOffsCorrn`
- `CalcBmwMotAgOffsSelnStSigInvld`
- `CalcBmwMotAgOffsSelnStIni`
- `BmwMotAgOffsSelnStTranCase`
- `BmwMotAgSelnStOffsCmpd`
- `BmwMotAgSelnStSigInvld`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_BmwHwAgArbnAndEotPosn.h`
- `BmwHwAgArbnAndEotPosn_Cfg.h`
- `ArchGlbPrm.h`
- `ElecGlbPrm.h`
- `SysGlbPrm.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `BmwHwAgArbnAndEotPosn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwHwAgArbnAndEotPosn_IntegrationManual](../cf071a_bmwhwagarbnandeotposn_impl__bmwhwagarbnandeotposn-integrationmanual-doc/)
- [BmwHwAgArbnAndEotPosn_MDD](../cf071a_bmwhwagarbnandeotposn_impl__bmwhwagarbnandeotposn-mdd-docx/)

Source files remain in the repository next to this documentation.

