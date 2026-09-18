---
title: 'CF070A BmwFltHndlg'
description: 'CF070A_BmwFltHndlg_Impl (ASW). Implementation of CF070A - BMW Fault Handling'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of CF070A - BMW Fault Handling

*Repository path:* `CF070A_BmwFltHndlg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwFltHndlg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BmwFltHndlgInit1`
- `BmwFltHndlgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwFltHndlg.h`
- `Dem.h`
- `BmwFltHndlg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwFltHndlg_IntegrationManual](../cf070a_bmwflthndlg_impl__bmwflthndlg-integrationmanual-doc/)
- [BmwFltHndlg_MDD](../cf070a_bmwflthndlg_impl__bmwflthndlg-mdd-docx/)

Source files remain in the repository next to this documentation.

