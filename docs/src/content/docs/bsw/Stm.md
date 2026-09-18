---
title: 'Stm Stm'
description: 'Stm (BSW). BMW State Monitor (BAC).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW State Monitor (BAC).

*Repository path:* `Stm/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 12 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (5 C file(s)) | `Stm.c`, `Stm_ComAdapter.c`, `Stm_ErrMemAdapter.c`, `Stm_MgmtAdapter.c`, `Stm_TimerAdapter.c` |
| `include/` (7 header(s)) | `Stm.h`, `Stm_Com.h`, `Stm_ErrMemAdapter.h`, `Stm_Mgmt.h`, `Stm_MgmtAdapter.h`, `Stm_Timer.h`, `Stm_Version.h` |
| `autosar/` (2 ARXML) | `StmClassic_paramdef.arxml`, `Stm_ext_interfaces.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 11):

- `Stm_Version.h`
- `Stm.h`
- `Stm_ErrMemAdapter.h`
- `Stm_MgmtAdapter.h`
- `Stm_MemMap.h`
- `Stm_Com.h`
- `Stm_Mgmt.h`
- `Stm_Timer.h`
- `Rte_Stm.h`
- `StmClassic_Version.h`
- `StmClassic_PBCfg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [StmClassic_IntegrationManual](../stm__stmclassic-integrationmanual-pdf/)
- [StmClassic_ReleaseNotes](../stm__stmclassic-releasenotes-pdf/)
- [StmClassic_RequirementsTable](../stm__stmclassic-requirementstable-pdf/)
- [StmGeneric_ReleaseNotes](../stm__stmgeneric-releasenotes-pdf/)
- [StmGeneric_RequirementsTable](../stm__stmgeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

