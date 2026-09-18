---
title: 'SF023A TunSelnAuthy'
description: 'SF023A_TunSelnAuthy_Impl (ASW). Header for TunSelnAuthy'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Header for TunSelnAuthy

*Repository path:* `SF023A_TunSelnAuthy_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `TunSelnAuthy.c` |
| `include/` (1 header(s)) | `TunSelnAuthy.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `RtCalChgReq_Oper`
- `TunSelnAuthyInit1`
- `XcpCalChgReq_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_TunSelnAuthy.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `TunSelnAuthy.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `TunSelnAuthy_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TunSelnAuthy_IntegrationManual](../sf023a_tunselnauthy_impl__tunselnauthy-integrationmanual-doc/)
- [TunSelnAuthy_MDD](../sf023a_tunselnauthy_impl__tunselnauthy-mdd-docx/)

Source files remain in the repository next to this documentation.

