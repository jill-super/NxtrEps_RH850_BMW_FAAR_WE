---
title: 'MM101A BmwMsgSlot68Bas0Repn2BusFrChA'
description: 'MM101A_BmwMsgSlot68Bas0Repn2BusFrChA_Impl (ASW). BMW Message Slot 68 Base 0 Repetition 2 Bus FlexRay Channel A Processing'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW Message Slot 68 Base 0 Repetition 2 Bus FlexRay Channel A Processing

*Repository path:* `MM101A_BmwMsgSlot68Bas0Repn2BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), renesas: 1 file(s), vector: 13 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot68Bas0Repn2BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `ClrNtcsAndCntrs`
- `Ntc121Procg`
- `Ntc122Procg`
- `Ntc123Procg`
- `Ntc124Procg`
- `Ntc125Procg`
- `Ntc126Procg`
- `Ntc127Procg`
- `Ntc128Procg`
- `Ntc129Procg`
- `Ntc12BProcg`
- `Ntc12CProcg`
- `Ntc12DProcg`
- `Ntc12EProcg`
- `Ntc12FProcg`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_BmwMsgSlot68Bas0Repn2BusFrChA.h`
- `NxtrMath.h`
- `E2EPW_BmwMsgSlot68Bas0Repn2BusFrChA_sigGroup_TAR_QTA_STRMOM_DV_sigGroup_TAR_QTA_STRMOM_DV_rx.h`
- `E2EPW_BmwMsgSlot68Bas0Repn2BusFrChA_sigGroup_TAR_STMOM_DV_ACT_sigGroup_TAR_STMOM_DV_ACT_rx.h`
- `BmwMsgSlot68Bas0Repn2BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

