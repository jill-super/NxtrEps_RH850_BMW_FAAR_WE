---
title: 'SF049B LoaMgr'
description: 'SF049B_LoaMgr_Impl (ASW). Implements LoaMgr (SF049B) FDD'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implements LoaMgr (SF049B) FDD

*Repository path:* `SF049B_LoaMgr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `LoaMgr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 13):

- `LtchInp`
- `CntMtgtnReq`
- `ReqHwTqResp`
- `ReqMotAgResp`
- `ReqCurrMeasResp`
- `ReqInvtrResp`
- `CntSwBasdMtgtnChk`
- `SelFinalResp`
- `SetFaults`
- `SwMtgtnEn`
- `LoaMgrCoder`
- `LoaMgrInit1`
- `LoaMgrPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_LoaMgr.h`
- `NxtrMath.h`
- `LoaMgr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [LoaMgr_IntegrationManual](../sf049b_loamgr_impl__loamgr-integrationmanual-doc/)
- [LoaMgr_MDD](../sf049b_loamgr_impl__loamgr-mdd-docx/)

Source files remain in the repository next to this documentation.

