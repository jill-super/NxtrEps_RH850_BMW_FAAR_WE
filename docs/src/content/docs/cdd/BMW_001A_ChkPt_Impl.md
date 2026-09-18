---
title: 'BMW BMW_001A_ChkPt'
description: 'BMW_001A_ChkPt_Impl (CDD). Check Point functions for BSW tasks'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Check Point functions for BSW tasks

*Repository path:* `BMW_001A_ChkPt_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 36 file(s), nexteer: 38 file(s), vector: 32 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (5 C file(s)) | `CDD_ChkPtAppl10.c`, `CDD_ChkPtAppl7.c`, `CDD_ChkPtAppl8.c`, `CDD_ChkPtAppl9.c`, `CDD_ChkPt_Bsw.c` |
| `include/` (1 header(s)) | `CDD_ChkPt_Bsw.h` |
| `autosar/` (4 ARXML) | `ChkPt_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `ChkPt_10msBswAppl10Strt`
- `ChkPt_10msBswAppl10End`
- `ChkPt_100msAppl10End`
- `ChkPt_100msAppl10Strt`
- `ChkPt_10msAppl10End`
- `ChkPt_10msAppl10Strt`
- `ChkPt_2msAAppl10End`
- `ChkPt_2msAAppl10Strt`
- `ChkPt_2msBAppl10End`
- `ChkPt_2msBAppl10Strt`
- `ChkPt_4msAppl10End`
- `ChkPt_4msAppl10Strt`
- `ChkPt_100msAppl7End`
- `ChkPt_100msAppl7Strt`
- `ChkPt_10msAppl7End`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Rte_CDD_ChkPtAppl10.h`
- `Os.h`
- `CDD_ChkPtAppl10_MemMap.h`
- `Rte_CDD_ChkPtAppl7.h`
- `CDD_ChkPtAppl7_MemMap.h`
- `Rte_CDD_ChkPtAppl8.h`
- `CDD_ChkPtAppl8_MemMap.h`
- `Rte_CDD_ChkPtAppl9.h`
- `CDD_ChkPtAppl9_MemMap.h`
- `Std_Types.h`
- `CDD_ChkPt_Bsw.h`
- `WdgM.h`
- `WdgM_PBcfg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ChkPt Integration Manual](../bmw_001a_chkpt_impl__chkpt-integration-manual-doc/)

Source files remain in the repository next to this documentation.

