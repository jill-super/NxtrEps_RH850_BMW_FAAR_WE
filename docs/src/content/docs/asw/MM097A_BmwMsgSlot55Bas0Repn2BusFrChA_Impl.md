---
title: 'MM097A BmwMsgSlot55Bas0Repn2BusFrChA'
description: 'MM097A_BmwMsgSlot55Bas0Repn2BusFrChA_Impl (ASW). Implementation of BmwMsgSlot55Bas0Repn2BusFrChA FDD MM097A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BmwMsgSlot55Bas0Repn2BusFrChA FDD MM097A

*Repository path:* `MM097A_BmwMsgSlot55Bas0Repn2BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), renesas: 1 file(s), vector: 13 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot55Bas0Repn2BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `ChkNtcSts`
- `ACLNY_MASSCNTR_Missing_Oper`
- `ACLNY_MASSCNTR_Received_Oper`
- `BmwMsgSlot55Bas0Repn2BusFrChAInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BmwMsgSlot55Bas0Repn2BusFrChA.h`
- `E2EPW_BmwMsgSlot55Bas0Repn2BusFrChA_sigGroup_ACLNY_MASSCNTR_sigGroup_ACLNY_MASSCNTR_rx.h`
- `NxtrMath.h`
- `BmwMsgSlot55Bas0Repn2BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

