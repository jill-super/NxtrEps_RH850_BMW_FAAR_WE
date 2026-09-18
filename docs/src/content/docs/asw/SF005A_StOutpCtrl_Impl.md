---
title: 'SF005A StOutpCtrl'
description: 'SF005A_StOutpCtrl_Impl (ASW). Implementation of State Output Control - FDD SF005A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of State Output Control - FDD SF005A

*Repository path:* `SF005A_StOutpCtrl_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `StOutpCtrl.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `RateLimit`
- `RateSource`
- `StOutpCtrlInit1`
- `StOutpCtrlPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_StOutpCtrl.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `StOutpCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [StOutpCtrl_IntegrationManual](../sf005a_stoutpctrl_impl__stoutpctrl-integrationmanual-doc/)
- [StOutpCtrl_MDD](../sf005a_stoutpctrl_impl__stoutpctrl-mdd-doc/)

Source files remain in the repository next to this documentation.

