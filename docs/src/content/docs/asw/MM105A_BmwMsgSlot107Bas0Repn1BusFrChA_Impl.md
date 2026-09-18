---
title: 'MM105A BmwMsgSlot107Bas0Repn1BusFrChA'
description: 'MM105A_BmwMsgSlot107Bas0Repn1BusFrChA_Impl (ASW). Implementation of BmwMsgSlot107Bas0Repn1BusFrChA FDD MM105A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BmwMsgSlot107Bas0Repn1BusFrChA FDD MM105A

*Repository path:* `MM105A_BmwMsgSlot107Bas0Repn1BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), renesas: 1 file(s), vector: 13 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot107Bas0Repn1BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `BmwMsgSlot107Bas0Repn1BusFrChAInit1`
- `OFFS_QUAD_EPS_Missing_Oper`
- `OFFS_QUAD_EPS_Received_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot107Bas0Repn1BusFrChA.h`
- `E2EPW_BmwMsgSlot107Bas0Repn1BusFrChA_sigGroup_OFFS_QUAD_EPS_sigGroup_OFFS_QUAD_EPS_rx.h`
- `BmwMsgSlot107Bas0Repn1BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

