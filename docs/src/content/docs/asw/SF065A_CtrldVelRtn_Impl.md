---
title: 'SF065A CtrldVelRtn'
description: 'SF065A_CtrldVelRtn_Impl (ASW). Implementation of Controlled Velocity Return SF109A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Controlled Velocity Return SF109A

*Repository path:* `SF065A_CtrldVelRtn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CtrldVelRtn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `DrvrTqSeln`
- `Dampg`
- `CtrldVelRtnInit1`
- `CtrldVelRtnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_CtrldVelRtn.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrFil.h`
- `ArchGlbPrm.h`
- `CtrldVelRtn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CtrldVelRtn_Integration Manual](../sf065a_ctrldvelrtn_impl__ctrldvelrtn-integration-manual-doc/)
- [CtrldVelRtn_MDD](../sf065a_ctrldvelrtn_impl__ctrldvelrtn-mdd-docx/)

Source files remain in the repository next to this documentation.

