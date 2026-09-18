---
title: 'SF043A TqOscn'
description: 'SF043A_TqOscn_Impl (ASW). Implementation of Torque Oscillation algorithm (FDD SF043A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Torque Oscillation algorithm (FDD SF043A)

*Repository path:* `SF043A_TqOscn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 10 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `TqOscn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `ChkFlg`
- `AmpRateLim`
- `TqOscnInit1`
- `TqOscnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_TqOscn.h`
- `NxtrFil.h`
- `NxtrFixdPt.h`
- `ArchGlbPrm.h`
- `NxtrMath.h`
- `FltInj.h`
- `TqOscn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TqOscn_IntegrationManual](../sf043a_tqoscn_impl__tqoscn-integrationmanual-doc/)
- [TqOscn_MDD](../sf043a_tqoscn_impl__tqoscn-mdd-docx/)

Source files remain in the repository next to this documentation.

