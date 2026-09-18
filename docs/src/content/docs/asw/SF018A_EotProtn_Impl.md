---
title: 'SF018A EotProtn'
description: 'SF018A_EotProtn_Impl (ASW). Implementation of End of Travel Protection function that specifies performance attributes'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of End of Travel Protection function that specifies performance attributes

*Repository path:* `SF018A_EotProtn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `EotProtn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 11):

- `EotVelImpct`
- `LimPosnDetd`
- `CalcEntrGain`
- `CalcExitGain`
- `CalcEotGain`
- `FildEotGain`
- `CalcEotDampg`
- `EotActvCmdCalc`
- `SoftEndStopStCtrl`
- `EotProtnInit1`
- `EotProtnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_EotProtn.h`
- `NxtrFil.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `NxtrFixdPt.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `EotProtn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [EotProtn_Integration Manual](../sf018a_eotprotn_impl__eotprotn-integration-manual-doc/)
- [EotProtn_MDD](../sf018a_eotprotn_impl__eotprotn-mdd-docx/)

Source files remain in the repository next to this documentation.

