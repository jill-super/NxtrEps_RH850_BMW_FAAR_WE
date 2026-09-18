---
title: 'ES311A GateDrv0Ctrl'
description: 'ES311A_GateDrv0Ctrl_Impl (CDD). Gate Drive 0 Control function responsible for configuration, deactivation and determination of fault status for Gate Dri'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Gate Drive 0 Control function responsible for configuration, deactivation and determination of fault status for Gate Drive 0.

*Repository path:* `ES311A_GateDrv0Ctrl_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 16 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `GateDrv0Ctrl.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `GateDrv0Ctrl_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `SpiAsyncTx`
- `OffStVrfySt`
- `OffStVrfyData`
- `CfgSt`
- `ReadBackRegs`
- `OperFltMonrSt`
- `GateDrvDetermineOnStSngFETFlt`
- `GateDrvDetermineVltgFlt`
- `GateDrvDetermineGenericFlt`
- `SetNtcStInfo`
- `ChkResVrfyRegs`
- `WriteOutput`
- `GateDrv0CtrlInit1`
- `GateDrv0CtrlPer1`
- `GateDrv0CtrlPer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_GateDrv0Ctrl.h`
- `ArchGlbPrm.h`
- `ElecGlbPrm.h`
- `Spi.h`
- `Os.h`
- `NxtrFil.h`
- `NxtrMath.h`
- `GateDrv0Ctrl_Cfg_private.h`
- `GateDrv0Ctrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [GateDrv0Ctrl_IntegrationManual](../es311a_gatedrv0ctrl_impl__gatedrv0ctrl-integrationmanual-doc/)
- [GateDrv0Ctrl_MDD](../es311a_gatedrv0ctrl_impl__gatedrv0ctrl-mdd-doc/)

Source files remain in the repository next to this documentation.

