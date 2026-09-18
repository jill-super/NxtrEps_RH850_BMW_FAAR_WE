---
title: 'SF105A MotCurrRegVltgLimr'
description: 'SF105A_MotCurrRegVltgLimr_Impl (ASW). Current Measurement Arbitration Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Current Measurement Arbitration Complex Driver Header

*Repository path:* `SF105A_MotCurrRegVltgLimr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 18 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_MotCurrRegVltgLimr.c`, `CDD_MotCurrRegVltgLimr_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_MotCurrRegVltgLimr.h`, `CDD_MotCurrRegVltgLimr_MotCtrl_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `MotCurrRegVltgLimrPer1`
- `MotCurrRegVltgLimrInit1`
- `KpKiCtrl`
- `ErrorCalcQax`
- `LoaScaFac`
- `MotCurr_Pred`
- `Decoder`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 10):

- `Rte_CDD_MotCurrRegVltgLimr.h`
- `NxtrFil.h`
- `ElecGlbPrm.h`
- `CDD_MotCurrRegVltgLimr_MemMap.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotCurrRegVltgLimr.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `MotRefMdl.h`
- `CDD_MotCurrRegVltgLimr_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotCurrRegVltgLimr_Integration Manual](../sf105a_motcurrregvltglimr_impl__motcurrregvltglimr-integration-manual-docx/)
- [MotCurrRegVltgLimr_MDD](../sf105a_motcurrregvltglimr_impl__motcurrregvltglimr-mdd-docx/)

Source files remain in the repository next to this documentation.

