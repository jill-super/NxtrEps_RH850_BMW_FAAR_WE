---
title: 'SF104A MotCurrRegCfg'
description: 'SF104A_MotCurrRegCfg_Impl (ASW). Implementation of MotCurrRegCfg'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of MotCurrRegCfg

*Repository path:* `SF104A_MotCurrRegCfg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotCurrRegCfg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `MotCurrRegCfgInit1`
- `MotCurrRegCfgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_MotCurrRegCfg.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `ArchGlbPrm.h`
- `NxtrFil.h`
- `MotCurrRegCfg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotCurrRegCfg_IntegrationManual](../sf104a_motcurrregcfg_impl__motcurrregcfg-integrationmanual-doc/)
- [MotCurrRegCfg_MDD](../sf104a_motcurrregcfg_impl__motcurrregcfg-mdd-doc/)

Source files remain in the repository next to this documentation.

