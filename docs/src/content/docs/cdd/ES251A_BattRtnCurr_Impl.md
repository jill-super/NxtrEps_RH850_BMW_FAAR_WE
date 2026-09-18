---
title: 'ES251A BattRtnCurr'
description: 'ES251A_BattRtnCurr_Impl (CDD). Battery Return Current measurement Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Battery Return Current measurement Header

*Repository path:* `ES251A_BattRtnCurr_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 17 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_BattRtnCurr.c`, `CDD_BattRtnCurr_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_BattRtnCurr.h`, `CDD_BattRtnCurr_MotCtrl_MemMap.h` |
| `autosar/` (4 ARXML) | `CDD_BattRtnCurr_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `BattRtnCurrPer1`
- `BattRtnCurrInit1`
- `BattRtnCurrPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_CDD_BattRtnCurr.h`
- `CDD_BattRtnCurr.h`
- `NxtrFil.h`
- `NxtrMath.h`
- `CDD_BattRtnCurr_MemMap.h`
- `CDD_BattRtnCurr_Cfg.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_BattRtnCurr_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BattRtnCurr_IntegrationManual](../es251a_battrtncurr_impl__battrtncurr-integrationmanual-doc/)
- [BattRtnCurr_MDD](../es251a_battrtncurr_impl__battrtncurr-mdd-docx/)

Source files remain in the repository next to this documentation.

