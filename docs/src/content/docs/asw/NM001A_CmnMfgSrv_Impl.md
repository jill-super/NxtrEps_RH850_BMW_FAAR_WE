---
title: 'NM001A CmnMfgSrv'
description: 'NM001A_CmnMfgSrv_Impl (ASW). Common Manufacturing Services Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Common Manufacturing Services Header

*Repository path:* `NM001A_CmnMfgSrv_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 199 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (186 C file(s)) | `CmnMfgSrv.c`, `CmnMfgSrvFct.c`, `SrvF000.c`, `SrvF001.c`, `SrvF002.c`, `SrvF010.c`, `SrvF100.c`, `SrvF101.c`, `SrvF110.c`, `SrvF111.c`, `SrvF112.c`, `SrvF113.c` |
| `include/` (3 header(s)) | `CmnMfgSrv.h`, `CmnMfgSrvFct.h`, `CmnMfgSrvTyp.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `NxtrMfgSrv_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `CmnMfgSrvFct_SynthesizeFloat`
- `CmnMfgSrvFct_DecomposeFloat`
- `CmnMfgSrvFct_Synthesize32`
- `CmnMfgSrvFct_Decompose32`
- `CmnMfgSrvFct_Synthesize16`
- `CmnMfgSrvFct_Decompose16`
- `CmnMfgSrv_SynthesizeDiBits`
- `CmnMfgSrv_DecomposeDiBits`
- `LoadPidTbl`
- `PerfLookup`
- `PerfLenChk`
- `PerfEnvChk`
- `PerfSrv`
- `ProcRspCod`
- `CmnMfgSrv_SrvF000RoutineStrt`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 10):

- `Rte_CmnMfgSrv.h`
- `CmnMfgSrv.h`
- `CmnMfgSrvTyp.h`
- `CmnMfgSrvFct.h`
- `MfgSrvCfg.h`
- `NxtrMath.h`
- `os.h`
- `CDD_ExcpnHndlg.h`
- `MemMap.h`
- `CmnMfgSrv_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

