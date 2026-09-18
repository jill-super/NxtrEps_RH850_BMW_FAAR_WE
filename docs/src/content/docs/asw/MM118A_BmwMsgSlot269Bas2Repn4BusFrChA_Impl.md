---
title: 'MM118A BmwMsgSlot269Bas2Repn4BusFrChA'
description: 'MM118A_BmwMsgSlot269Bas2Repn4BusFrChA_Impl (ASW). BMW Message Slot 269 Base 2 Repetition 4 Bus FlexRay Channel A Processing (MM118A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW Message Slot 269 Base 2 Repetition 4 Bus FlexRay Channel A Processing (MM118A)

*Repository path:* `MM118A_BmwMsgSlot269Bas2Repn4BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot269Bas2Repn4BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 8):

- `ClrNtcsAndCntrs`
- `AllNtcProcg`
- `Ntc163Procg`
- `Ntc162Procg`
- `Ntc161Procg`
- `BmwMsgSlot269Bas2Repn4BusFrChA_Init`
- `CTR_VIB_STW_DISP_EXMI_SP2015_Missing`
- `CTR_VIB_STW_DISP_EXMI_SP2015_Received`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Rte_BmwMsgSlot269Bas2Repn4BusFrChA.h`
- `BmwMsgSlot269Bas2Repn4BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

