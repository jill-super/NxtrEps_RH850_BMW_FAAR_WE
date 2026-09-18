---
title: 'CF084A BmwDiagcSrvHndlg'
description: 'CF084A_BmwDiagcSrvHndlg_Impl (ASW). BMW Diagnostics Services Hanlder'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW Diagnostics Services Hanlder

*Repository path:* `CF084A_BmwDiagcSrvHndlg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwDiagcSrvHndlg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 12):

- `HwAgOrHwVelChk`
- `OperStChk`
- `HandsOnDetn`
- `ChkRoutineCdn`
- `SnsrCdnChk`
- `BmwDiagcSrvFHndlMileageRead_Oper`
- `BmwDiagcSrvFHndlgAmbTRead_Oper`
- `BmwDiagcSrvFHndlgEpsBaseNwRead_Oper`
- `BmwDiagcSrvFHndlgEpsBattVltgRead_Oper`
- `BmwDiagcSrvFHndlgEpsFactryIninRes_Oper`
- `BmwDiagcSrvFHndlgEpsFactryIninStop_Oper`
- `BmwDiagcSrvFHndlgEpsFactryIninStrt_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_BmwDiagcSrvHndlg.h`
- `Os.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `Dlog_User.h`
- `BmwDiagcSrvHndlg_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

