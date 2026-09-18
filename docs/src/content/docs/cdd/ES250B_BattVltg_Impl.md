---
title: 'ES250B BattVltg'
description: 'ES250B_BattVltg_Impl (CDD). Implementation of Battery Voltage measurement for single inverter design (ES250B)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Battery Voltage measurement for single inverter design (ES250B)

*Repository path:* `ES250B_BattVltg_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BattVltg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BattVltgInit1`
- `BattVltgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BattVltg.h`
- `NxtrMath.h`
- `BattVltg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BattVltg_IntegrationManual](../es250b_battvltg_impl__battvltg-integrationmanual-doc/)
- [BattVltg_MDD](../es250b_battvltg_impl__battvltg-mdd-docx/)

Source files remain in the repository next to this documentation.

