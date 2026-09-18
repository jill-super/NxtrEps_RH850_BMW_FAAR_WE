---
title: 'ES004A PwrUpSeq'
description: 'ES004A_PwrUpSeq_Impl (CDD). Power Up Sequence'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Power Up Sequence

*Repository path:* `ES004A_PwrUpSeq_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PwrUpSeq.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `PwrTurnOffCtrl_Oper`
- `PwrUpSeqInit1`
- `PwrUpSeqPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_PwrUpSeq.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `PwrUpSeq_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PwrUpSeq_IntegrationManual](../es004a_pwrupseq_impl__pwrupseq-integrationmanual-doc/)
- [PwrUpSeq_MDD](../es004a_pwrupseq_impl__pwrupseq-mdd-doc/)

Source files remain in the repository next to this documentation.

