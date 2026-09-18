---
title: 'DF002A Swp'
description: 'DF002A_Swp_Impl (CDD). Fault Injection definitions'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Fault Injection definitions

*Repository path:* `DF002A_Swp_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Swp.c` |
| `include/` (1 header(s)) | `Swp.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `SwpInit1`
- `SwpPer1`
- `SwpPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_Swp.h`
- `Swp.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `Swp_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Swp_IntegrationManual](../df002a_swp_impl__swp-integrationmanual-doc/)
- [Swp_MDD](../df002a_swp_impl__swp-mdd-docx/)

Source files remain in the repository next to this documentation.

