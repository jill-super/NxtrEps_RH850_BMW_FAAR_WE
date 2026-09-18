---
title: 'NM010B ProgMfgSrv'
description: 'NM010B_ProgMfgSrv_Impl (ASW). BMW specific manufacturing services'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW specific manufacturing services

*Repository path:* `NM010B_ProgMfgSrv_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `ProgMfgSrv.c`, `SrvFED0.c`, `SrvFED1.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `ProgMfgSrvInit1`
- `ProgMfgSrv_SrvFED0Rd`
- `ProgMfgSrv_SrvFED0Wr`
- `ProgMfgSrv_SrvFED1Rd`
- `ProgMfgSrv_SrvFED1Wr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_ProgMfgSrv.h`
- `ProgMfgSrv_MemMap.h`
- `CmnMfgSrv.h`
- `CmnMfgSrvTyp.h`
- `MfgSrvCfg.h`

## Documents

No Word/PDF documents were found for this module.

