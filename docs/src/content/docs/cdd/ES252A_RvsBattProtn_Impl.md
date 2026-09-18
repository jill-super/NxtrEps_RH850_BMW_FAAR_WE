---
title: 'ES252A RvsBattProtn'
description: 'ES252A_RvsBattProtn_Impl (CDD). Implementation of Reverse Battery Protection FDD ES252A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Reverse Battery Protection FDD ES252A

*Repository path:* `ES252A_RvsBattProtn_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `RvsBattProtn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml`, `RvsBattProtn_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `RvsBattProtnInit1`
- `RvsBattProtnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_RvsBattProtn.h`
- `RvsBattProtn_Cfg.h`
- `RvsBattProtn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [RvsBattProtn_IntegrationManual](../es252a_rvsbattprotn_impl__rvsbattprotn-integrationmanual-doc/)
- [RvsBattProtn_MDD](../es252a_rvsbattprotn_impl__rvsbattprotn-mdd-docx/)

Source files remain in the repository next to this documentation.

