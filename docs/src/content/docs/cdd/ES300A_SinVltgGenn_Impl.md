---
title: 'ES300A SinVltgGenn'
description: 'ES300A_SinVltgGenn_Impl (CDD). Sine Voltage Generation header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Sine Voltage Generation header

*Repository path:* `ES300A_SinVltgGenn_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 18 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_SinVltgGenn.c`, `CDD_SinVltgGenn_MotCtrl.c` |
| `include/` (3 header(s)) | `CDD_SinVltgGenn.h`, `CDD_SinVltgGenn_MotCtrl_MemMap.h`, `CDD_SinVltgGenn_private.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `SinVltgGennPer1`
- `SinVltgGennPer2`
- `SinVltgGennInit1`
- `ModIndxPhaCalc`
- `PhaOnTiCalc`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_CDD_SinVltgGenn.h`
- `ElecGlbPrm.h`
- `CDD_SinVltgGenn_private.h`
- `CDD_SinVltgGenn_MemMap.h`
- `CDD_SinVltgGenn.h`
- `CDD_MotCtrlMgr_Data.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `CDD_SinVltgGenn_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [SinVltgGenn_IntegrationManual](../es300a_sinvltggenn_impl__sinvltggenn-integrationmanual-doc/)
- [SinVltgGenn_MDD](../es300a_sinvltggenn_impl__sinvltggenn-mdd-doc/)

Source files remain in the repository next to this documentation.

