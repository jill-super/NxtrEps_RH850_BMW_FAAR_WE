---
title: 'CM455A Tauj0CfgAndUse'
description: 'CM455A_Tauj0CfgAndUse_Impl (CDD). Implementation of Tauj0 Configuration and Use FDD CM455A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Tauj0 Configuration and Use FDD CM455A

*Repository path:* `CM455A_Tauj0CfgAndUse_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_Tauj0CfgAndUse.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `Tauj0CfgAndUseInit1`
- `Tauj0CfgAndUsePer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_CDD_Tauj0CfgAndUse.h`
- `tauj_regs.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `CDD_Tauj0CfgAndUse_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Tauj0CfgAndUse_IntegrationManual](../cm455a_tauj0cfganduse_impl__tauj0cfganduse-integrationmanual-doc/)
- [Tauj0CfgAndUse_MDD](../cm455a_tauj0cfganduse_impl__tauj0cfganduse-mdd-docx/)

Source files remain in the repository next to this documentation.

