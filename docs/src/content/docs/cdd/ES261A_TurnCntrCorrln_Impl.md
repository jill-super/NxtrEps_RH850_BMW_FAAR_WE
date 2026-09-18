---
title: 'ES261A TurnCntrCorrln'
description: 'ES261A_TurnCntrCorrln_Impl (CDD). Implementation of Turns counter correlation (ES261A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Turns counter correlation (ES261A)

*Repository path:* `ES261A_TurnCntrCorrln_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `TurnCntrCorrln.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `CorrlnSigAvlChk`
- `TurnCntrCorrlnInit1`
- `TurnCntrCorrlnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_TurnCntrCorrln.h`
- `NxtrMath.h`
- `TurnCntrCorrln_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TurnCntrCorrln_IntegrationManual](../es261a_turncntrcorrln_impl__turncntrcorrln-integrationmanual-doc/)
- [TurnCntrCorrln_MDD](../es261a_turncntrcorrln_impl__turncntrcorrln-mdd-doc/)

Source files remain in the repository next to this documentation.

