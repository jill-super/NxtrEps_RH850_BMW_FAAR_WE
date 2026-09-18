---
title: 'ES104B XcpIf'
description: 'ES104B_XcpIf_Impl (CDD). Private header file for XCP Interface ES 104A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Private header file for XCP Interface ES 104A

*Repository path:* `ES104B_XcpIf_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 12 file(s), nexteer: 20 file(s), vector: 11 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_XcpIf.c` |
| `include/` (2 header(s)) | `CDD_XcpIf_private.h`, `XcpAppl.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml`, `XcpIf_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `XcpAppl_GetTimestamp`
- `XcpAppl_MemCpy`
- `XcpAppl_MeasurementRead`
- `XcpAppl_CalibrationWrite`
- `XcpAppl_GetPointer`
- `XcpAppl_CheckReadAccess`
- `XcpAppl_CalculateChecksum`
- `XcpAppl_OpenCmdIf`
- `XcpAppl_GetSeed`
- `XcpAppl_Unlock`
- `XcpAppl_SetCalPage`
- `XcpAppl_GetCalPage`
- `XcpAppl_CopyCalPage`
- `XcpAppl_UserService`
- `XcpAppl_ConStateNotification`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_CDD_XcpIf.h`
- `CDD_XcpIf_private.h`
- `CDD_XcpIf_Cfg_private.h`
- `CDD_XcpIf_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [XcpIf_Integration_Manual](../es104b_xcpif_impl__xcpif-integration-manual-docx/)

Source files remain in the repository next to this documentation.

