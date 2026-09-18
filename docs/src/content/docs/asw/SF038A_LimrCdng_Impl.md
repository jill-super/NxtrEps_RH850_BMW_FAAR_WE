---
title: 'SF038A LimrCdng'
description: 'SF038A_LimrCdng_Impl (ASW). Implementation of Limiter Conditioning FDD SF038A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Limiter Conditioning FDD SF038A

*Repository path:* `SF038A_LimrCdng_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `LimrCdng.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `LimrCdngPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_LimrCdng.h`
- `ArchGlbPrm.h`
- `FltInj.h`
- `SysGlbPrm.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `LimrCdng_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [LimrCdng_IntegrationManual](../sf038a_limrcdng_impl__limrcdng-integrationmanual-doc/)
- [LimrCdng_MDD](../sf038a_limrcdng_impl__limrcdng-mdd-docx/)

Source files remain in the repository next to this documentation.

