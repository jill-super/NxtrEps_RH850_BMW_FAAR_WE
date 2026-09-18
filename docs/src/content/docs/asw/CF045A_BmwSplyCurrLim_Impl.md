---
title: 'CF045A BmwSplyCurrLim'
description: 'CF045A_BmwSplyCurrLim_Impl (ASW). BMW Supply Current Limit'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW Supply Current Limit

*Repository path:* `CF045A_BmwSplyCurrLim_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwSplyCurrLim.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `VltgDptCurrLim`
- `BmwSplyCurrLimInit1`
- `BmwSplyCurrLimPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_BmwSplyCurrLim.h`
- `ArchGlbPrm.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `BmwSplyCurrLim_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwSplyCurrLim_IntegrationManual](../cf045a_bmwsplycurrlim_impl__bmwsplycurrlim-integrationmanual-doc/)
- [BmwSplyCurrLim_MDD](../cf045a_bmwsplycurrlim_impl__bmwsplycurrlim-mdd-docx/)

Source files remain in the repository next to this documentation.

