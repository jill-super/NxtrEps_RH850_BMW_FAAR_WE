---
title: 'SF109A ElecPwrCns'
description: 'SF109A_ElecPwrCns_Impl (ASW). Implementation of Electric Power Consumption SF109A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Electric Power Consumption SF109A

*Repository path:* `SF109A_ElecPwrCns_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `ElecPwrCns.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `ElecPwrCnsPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_ElecPwrCns.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `ElecPwrCns_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ElecPwrCns_IntegrationManual](../sf109a_elecpwrcns_impl__elecpwrcns-integrationmanual-doc/)
- [ElecPwrCns_MDD](../sf109a_elecpwrcns_impl__elecpwrcns-mdd-doc/)

Source files remain in the repository next to this documentation.

