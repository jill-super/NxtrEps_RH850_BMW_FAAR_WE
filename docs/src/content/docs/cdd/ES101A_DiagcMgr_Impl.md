---
title: 'ES101A DiagcMgr'
description: 'ES101A_DiagcMgr_Impl (CDD). DiagcMgr header file for the DiagcMgr and DiagcMgrProxy components'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

DiagcMgr header file for the DiagcMgr and DiagcMgrProxy components

*Repository path:* `ES101A_DiagcMgr_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 130 file(s), nexteer: 163 file(s), vector: 117 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (15 C file(s)) | `DiagcMgr.c`, `DiagcMgrNonRTE.c`, `DiagcMgrProxyAppl0.c`, `DiagcMgrProxyAppl1.c`, `DiagcMgrProxyAppl10.c`, `DiagcMgrProxyAppl2.c`, `DiagcMgrProxyAppl3.c`, `DiagcMgrProxyAppl4.c`, `DiagcMgrProxyAppl5.c`, `DiagcMgrProxyAppl6.c`, `DiagcMgrProxyAppl7.c`, `DiagcMgrProxyAppl8.c` |
| `include/` (3 header(s)) | `DiagcMgr.h`, `DiagcMgrStaticTypes.h`, `DiagcMgr_private.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `DiagcMgr_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `DiagcMgrPwrDwn`
- `RestoreNtcFltAryDft`
- `RestoreSnpshtAryDft`
- `RestoreDiagcMgrLtchCntrAryDft`
- `UpdDtcEnaCdn`
- `GetNtcActv0_Oper`
- `GetNtcQlfrSts0_Oper`
- `SetNtcSts0_Oper`
- `SetNtcStsAndSnpshtData0_Oper`
- `GetNtcActv1_Oper`
- `GetNtcQlfrSts1_Oper`
- `SetNtcSts1_Oper`
- `SetNtcStsAndSnpshtData1_Oper`
- `GetNtcActv2_Oper`
- `GetNtcQlfrSts2_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Rte_DiagcMgr.h`
- `Dem.h`
- `DiagcMgr.h`
- `DiagcMgr_private.h`
- `NxtrDet.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `MemMap.h`
- `DiagcMgr_MemMap.h`
- `CDD_NvMProxy.h`
- `NvM.h`
- `DiagcMgrStaticTypes.h`
- `Rte_DiagcMgrProxyAppl0.h`
- `DiagcMgrProxyAppl0_MemMap.h`
- `Rte_DiagcMgrProxyAppl1.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DiagcMgrProxy_MDD](../es101a_diagcmgr_impl__diagcmgrproxy-mdd-doc/)
- [DiagcMgr_IntegrationManual](../es101a_diagcmgr_impl__diagcmgr-integrationmanual-doc/)
- [DiagcMgr_MDD](../es101a_diagcmgr_impl__diagcmgr-mdd-doc/)

Source files remain in the repository next to this documentation.

