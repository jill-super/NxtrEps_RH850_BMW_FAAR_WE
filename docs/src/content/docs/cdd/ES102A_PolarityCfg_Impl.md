---
title: 'ES102A PolarityCfg'
description: 'ES102A_PolarityCfg_Impl (CDD). Implementation of Polarity Configuration FDD ES102A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Polarity Configuration FDD ES102A

*Repository path:* `ES102A_PolarityCfg_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PolarityCfg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `GetPolarity`
- `PolarityCfgInit1`
- `PolarityCfgRead_Oper`
- `PolarityCfgWr_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Rte_PolarityCfg.h`
- `PolarityCfg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PolarityCfg_Integration Manual](../es102a_polaritycfg_impl__polaritycfg-integration-manual-docx/)
- [PolarityCfg_MDD](../es102a_polaritycfg_impl__polaritycfg-mdd-docx/)

Source files remain in the repository next to this documentation.

