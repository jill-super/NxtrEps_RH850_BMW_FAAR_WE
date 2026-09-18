---
title: 'MM529A BmwMsgSlot274Bas2Repn4BusFrChA'
description: 'MM529A_BmwMsgSlot274Bas2Repn4BusFrChA_Impl (ASW). Implementation of BMW Message Slot 274 Base 2 Repetition 4 Bus FlexRay Channel A MM523A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BMW Message Slot 274 Base 2 Repetition 4 Bus FlexRay Channel A MM523A

*Repository path:* `MM529A_BmwMsgSlot274Bas2Repn4BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), renesas: 1 file(s), vector: 14 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot274Bas2Repn4BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BmwMsgSlot274Bas2Repn4BusFrChAInit1`
- `BmwMsgSlot274Bas2Repn4BusFrChAPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot274Bas2Repn4BusFrChA.h`
- `E2EPW_BmwMsgSlot274Bas2Repn4BusFrChA_sigGroup_DISP_CC_EPS_sigGroup_DISP_CC_EPS_tx.h`
- `BmwMsgSlot274Bas2Repn4BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

