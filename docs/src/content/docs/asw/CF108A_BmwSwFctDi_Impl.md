---
title: 'CF108A BmwSwFctDi'
description: 'CF108A_BmwSwFctDi_Impl (ASW). Implementation of BMW Software Function Defeat (CF0108A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW Software Function Defeat (CF0108A)

*Repository path:* `CF108A_BmwSwFctDi_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 1 file(s), gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwSwFctDi.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 9):

- `OvrdCmdEna`
- `CtrldVelRtnEna`
- `ClsdLoopHysEna`
- `InertiaCmpVelCmdDiBmwOvrd`
- `PullCmpCmdDiBmwOvrd`
- `UpdCodingBits`
- `ReadCodingData`
- `BmwSwFctDiInit1`
- `BmwSwFctDiPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_BmwSwFctDi.h`
- `NxtrMath.h`
- `SysGlbPrm.h`
- `Coding.h`
- `BmwSwFctDi_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwSwFctDi_IntegrationManual](../cf108a_bmwswfctdi_impl__bmwswfctdi-integrationmanual-doc/)
- [BmwSwFctDi_MDD](../cf108a_bmwswfctdi_impl__bmwswfctdi-mdd-docx/)

Source files remain in the repository next to this documentation.

