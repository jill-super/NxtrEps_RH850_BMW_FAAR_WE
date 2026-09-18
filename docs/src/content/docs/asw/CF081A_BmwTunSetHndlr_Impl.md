---
title: 'CF081A BmwTunSetHndlr'
description: 'CF081A_BmwTunSetHndlr_Impl (ASW). CF081A Implementation'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CF081A Implementation

*Repository path:* `CF081A_BmwTunSetHndlr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwTunSetHndlr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `BmwTunSetHndlr_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `BmwTunSetHndlrInit1`
- `BmwTunSetHndlrPer1`
- `MotVrntRead_Oper`
- `MotVrntWr_Oper`
- `TunVrntRead_Oper`
- `TunVrntWr_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BmwTunSetHndlr.h`
- `BmwTunSetHndlr_Cfg.h`
- `NxtrMath.h`
- `BmwTunSetHndlr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwTunSetHndlr_IntegrationManual](../cf081a_bmwtunsethndlr_impl__bmwtunsethndlr-integrationmanual-doc/)
- [BmwTunSetHndlr_MDD](../cf081a_bmwtunsethndlr_impl__bmwtunsethndlr-mdd-docx/)

Source files remain in the repository next to this documentation.

