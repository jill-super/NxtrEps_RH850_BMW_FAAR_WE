---
title: 'SF017A HiLoadStallLimr'
description: 'SF017A_HiLoadStallLimr_Impl (ASW). Implementation of High load thermal management algorithm (FDD SF017A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of High load thermal management algorithm (FDD SF017A)

*Repository path:* `SF017A_HiLoadStallLimr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 13 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `HiLoadStallLimr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `HiLoadStallLimrInit1`
- `HiLoadStallLimrPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_HiLoadStallLimr.h`
- `NxtrMath.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `SysGlbPrm.h`
- `HiLoadStallLimr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HiLoadStallLimr_IntegrationManual](../sf017a_hiloadstalllimr_impl__hiloadstalllimr-integrationmanual-doc/)
- [HiLoadStallLimr_MDD](../sf017a_hiloadstalllimr_impl__hiloadstalllimr-mdd-docx/)

Source files remain in the repository next to this documentation.

