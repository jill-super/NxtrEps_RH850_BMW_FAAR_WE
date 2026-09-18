---
title: 'ES006A NvM'
description: 'ES006A_NvM_Impl (CDD). Header file for NvM Proxy component'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Header file for NvM Proxy component

*Repository path:* `ES006A_NvM_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 19 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `CDD_NvMProxy.c`, `CDD_NvMProxyApi.c`, `CDD_NvMProxyNonRte.c` |
| `include/` (1 header(s)) | `CDD_NvMProxy.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `NvMProxy_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `NvMProxy_Init0`
- `NvMProxy_MainFunction`
- `NvMProxy_ClsChkWr_Oper`
- `NvMProxy_EraseNvBlock`
- `NvMProxy_GetDataIndex`
- `NvMProxy_GetErrorStatus`
- `NvMProxy_InvalidateNvBlock`
- `NvMProxy_ReadBlock`
- `NvMProxy_RestoreBlockDefaults`
- `NvMProxy_SetBlockProtection`
- `NvMProxy_SetDataIndex`
- `NvMProxy_SetRamBlockStatus`
- `NvMProxy_WriteBlock`
- `NvMProxyInit1`
- `NONTRUSTED_NtWrapS_NvM_EraseNvBlock`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_NvMProxy.h`
- `CDD_NvMProxy_Cfg_private.h`
- `CDD_NvMProxy_MemMap.h`
- `NvM.h`
- `Os.h`
- `CDD_NvMProxy.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ES006A_NvM_Integration_Manual](../es006a_nvm_impl__es006a-nvm-integration-manual-doc/)

Source files remain in the repository next to this documentation.

