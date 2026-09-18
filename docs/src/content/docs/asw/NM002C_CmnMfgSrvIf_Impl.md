---
title: 'NM002C CmnMfgSrvIf'
description: 'NM002C_CmnMfgSrvIf_Impl (ASW). Implementation of common manufacturing service interface between DCM and NM001A.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of common manufacturing service interface between DCM and NM001A.

*Repository path:* `NM002C_CmnMfgSrvIf_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CmnMfgSrvIf.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `CmnMfgSrvIf_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `CmnMfgSrvIfInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Rte_CmnMfgSrvIf.h`
- `CmnMfgSrvIf_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CmnMfgSrvIf_IntegrationManual](../nm002c_cmnmfgsrvif_impl__cmnmfgsrvif-integrationmanual-docx/)

Source files remain in the repository next to this documentation.

