---
title: 'MM096A BmwMsgSlot53Bas3Repn8BusFrChA'
description: 'MM096A_BmwMsgSlot53Bas3Repn8BusFrChA_Impl (ASW). Implementation of BmwMsgSlot53Bas3Repn8BusFrChA FDD MM096A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of BmwMsgSlot53Bas3Repn8BusFrChA FDD MM096A

*Repository path:* `MM096A_BmwMsgSlot53Bas3Repn8BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot53Bas3Repn8BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `BmwRtIdxVldChk`
- `BmwSteerMdfnFacStsChk`
- `ClrCntrAndNtc`
- `BmwMsgSlot53Bas3Repn8BusFrChAInit1`
- `SU_CLE_DRDY_DXP_Miss`
- `SU_CLE_DRDY_DXP_Rxd`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot53Bas3Repn8BusFrChA.h`
- `NxtrMath.h`
- `BmwMsgSlot53Bas3Repn8BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

