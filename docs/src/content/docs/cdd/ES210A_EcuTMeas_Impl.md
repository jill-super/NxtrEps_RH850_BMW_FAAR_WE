---
title: 'ES210A EcuTMeas'
description: 'ES210A_EcuTMeas_Impl (CDD). Implementation of Ecu Temperature Measurement FDD ES210A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Ecu Temperature Measurement FDD ES210A

*Repository path:* `ES210A_EcuTMeas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 15 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `EcuTMeas.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `EcuTMeas_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `EcuTMeasInit1`
- `EcuTMeasPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_EcuTMeas.h`
- `NxtrMath.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `ArchGlbPrm.h`
- `EcuTMeas_Cfg_private.h`
- `EcuTMeas_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [EcuTMeas_IntegrationManual](../es210a_ecutmeas_impl__ecutmeas-integrationmanual-doc/)
- [EcuTMeas_MDD](../es210a_ecutmeas_impl__ecutmeas-mdd-docx/)

Source files remain in the repository next to this documentation.

