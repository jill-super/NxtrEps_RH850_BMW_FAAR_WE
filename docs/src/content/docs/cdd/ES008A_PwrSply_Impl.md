---
title: 'ES008A PwrSply'
description: 'ES008A_PwrSply_Impl (CDD). Power Supply Diagnostics Function - ES008A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Power Supply Diagnostics Function - ES008A

*Repository path:* `ES008A_PwrSply_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PwrSply.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `SpiAsyncTx`
- `PwrSplyInit1`
- `PwrSplyPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_PwrSply.h`
- `Spi.h`
- `Os.h`
- `PwrSply_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PwrSply_IntegrationManual](../es008a_pwrsply_impl__pwrsply-integrationmanual-doc/)
- [PwrSply_MDD](../es008a_pwrsply_impl__pwrsply-mdd-doc/)

Source files remain in the repository next to this documentation.

