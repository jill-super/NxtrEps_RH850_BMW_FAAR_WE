---
title: 'ES330A PhaDiscnct'
description: 'ES330A_PhaDiscnct_Impl (CDD). Phase Disconnect provides mechanism of disconnecting Motor Phases from system'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Phase Disconnect provides mechanism of disconnecting Motor Phases from system

*Repository path:* `ES330A_PhaDiscnct_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PhaDiscnct.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 9):

- `PerformDiag`
- `ClosingStateBody`
- `ClosedStateBody`
- `OpeningStateBody`
- `OpenedStateBody`
- `SetHwPhaDiscnctIO`
- `PhaDiscnctInit1`
- `PhaDiscnctPer1`
- `PhaDiscnctPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_PhaDiscnct.h`
- `ElecGlbPrm.h`
- `NxtrMath.h`
- `PhaDiscnct_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PhaDiscnct_IntegrationManual](../es330a_phadiscnct_impl__phadiscnct-integrationmanual-doc/)
- [PhaDiscnct_MDD](../es330a_phadiscnct_impl__phadiscnct-mdd-docx/)

Source files remain in the repository next to this documentation.

