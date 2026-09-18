---
title: 'MM098A BmwMsgSlot55Bas3Repn4BusFrChA'
description: 'MM098A_BmwMsgSlot55Bas3Repn4BusFrChA_Impl (ASW). Implementation of BmwMsgSlot55Bas3Repn4BusFrChA FDD MM098A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BmwMsgSlot55Bas3Repn4BusFrChA FDD MM098A

*Repository path:* `MM098A_BmwMsgSlot55Bas3Repn4BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), renesas: 1 file(s), vector: 13 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot55Bas3Repn4BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `BmwMsgSlot55Bas3Repn4BusFrChAInit1`
- `V_VEH_Missing_Oper`
- `V_VEH_Received_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot55Bas3Repn4BusFrChA.h`
- `E2EPW_BmwMsgSlot55Bas3Repn4BusFrChA_sigGroup_V_VEH_sigGroup_V_VEH_rx.h`
- `BmwMsgSlot55Bas3Repn4BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

