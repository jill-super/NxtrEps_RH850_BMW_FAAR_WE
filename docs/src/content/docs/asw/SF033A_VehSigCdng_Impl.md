---
title: 'SF033A VehSigCdng'
description: 'SF033A_VehSigCdng_Impl (ASW). Implementation of VehSigCdng FDD SF033A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of VehSigCdng FDD SF033A

*Repository path:* `SF033A_VehSigCdng_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `VehSigCdng.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `VehSigCdng_VehSpd`
- `VehSigCdng_VehLgtA`
- `VehSigCdng_VehLatA`
- `VehSigCdng_VehYawRate`
- `VehSigCdng_LatAEstmn`
- `VehSigCdngInit1`
- `VehSigCdngPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_VehSigCdng.h`
- `NxtrFil.h`
- `ArchGlbPrm.h`
- `FltInj.h`
- `NxtrMath.h`
- `VehSigCdng_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [VehSigCdng_Integration Manual](../sf033a_vehsigcdng_impl__vehsigcdng-integration-manual-doc/)
- [VehSigCdng_MDD](../sf033a_vehsigcdng_impl__vehsigcdng-mdd-docx/)

Source files remain in the repository next to this documentation.

