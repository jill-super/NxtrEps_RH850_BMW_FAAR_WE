---
title: 'MM526A BmwMsgSlot234Bas1Repn2BusFrChA'
description: 'MM526A_BmwMsgSlot234Bas1Repn2BusFrChA_Impl (ASW). Implementation of BMW Message Slot 234 Base 1 Repetition 2 Bus FlexRay Channel A MM526A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW Message Slot 234 Base 1 Repetition 2 Bus FlexRay Channel A MM526A

*Repository path:* `MM526A_BmwMsgSlot234Bas1Repn2BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), renesas: 1 file(s), vector: 14 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot234Bas1Repn2BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BmwMsgSlot234Bas1Repn2BusFrChAInit1`
- `BmwMsgSlot234Bas1Repn2BusFrChAPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot234Bas1Repn2BusFrChA.h`
- `E2EPW_BmwMsgSlot234Bas1Repn2BusFrChA_sigGroup_ST_EST_sigGroup_ST_EST_tx.h`
- `BmwMsgSlot234Bas1Repn2BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

