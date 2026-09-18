---
title: 'ES228B HwTqArbn'
description: 'ES228B_HwTqArbn_Impl (CDD). Arbitration between multiple Torque sensors and calculation of handwheel torque.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Arbitration between multiple Torque sensors and calculation of handwheel torque.

*Repository path:* `ES228B_HwTqArbn_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `HwTqArbn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `SigAvlChkRev`
- `HwTqArbnInit1`
- `HwTqArbnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_HwTqArbn.h`
- `NxtrMath.h`
- `HwTqArbn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HwTqArbn_Integration Manual](../es228b_hwtqarbn_impl__hwtqarbn-integration-manual-doc/)
- [HwTqArbn_MDD](../es228b_hwtqarbn_impl__hwtqarbn-mdd-docx/)

Source files remain in the repository next to this documentation.

