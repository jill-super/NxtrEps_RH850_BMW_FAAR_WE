---
title: 'SF069A HwRefTqSum'
description: 'SF069A_HwRefTqSum_Impl (ASW). Handwheel Reference Torque Summation is used to do the sum of reference'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Handwheel Reference Torque Summation is used to do the sum of reference

*Repository path:* `SF069A_HwRefTqSum_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `HwRefTqSum.c` |
| `include/` (1 header(s)) | `HwRefTqSum.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `HwRefTqSumInit1`
- `HwRefTqSumPer1`
- `HwRefTqSum_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `HwRefTqSum.h`
- `HwRefTqSum_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HwRefTqSum_IntegrationManual](../sf069a_hwreftqsum_impl__hwreftqsum-integrationmanual-doc/)
- [HwRefTqSum_MDD](../sf069a_hwreftqsum_impl__hwreftqsum-mdd-doc/)

Source files remain in the repository next to this documentation.

