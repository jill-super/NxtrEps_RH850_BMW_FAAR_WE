---
title: 'MM102A BmwMsgSlot68Bas1Repn2BusFrChA'
description: 'MM102A_BmwMsgSlot68Bas1Repn2BusFrChA_Impl (ASW). Implementation of BmwMsgSlot68Bas1Repn2BusFrChA FDD MM102A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BmwMsgSlot68Bas1Repn2BusFrChA FDD MM102A

*Repository path:* `MM102A_BmwMsgSlot68Bas1Repn2BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), renesas: 1 file(s), vector: 13 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot68Bas1Repn2BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `ChkNtcSts`
- `BmwMsgSlot68Bas1Repn2BusFrChAInit1`
- `ENERG_DGR_DRDY_Missing_Oper`
- `ENERG_DGR_DRDY_Received_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_BmwMsgSlot68Bas1Repn2BusFrChA.h`
- `E2EPW_BmwMsgSlot68Bas1Repn2BusFrChA_sigGroup_ENERG_DGR_DRDY_sigGroup_ENERG_DGR_DRDY_rx.h`
- `NxtrMath.h`
- `BmwMsgSlot68Bas1Repn2BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

