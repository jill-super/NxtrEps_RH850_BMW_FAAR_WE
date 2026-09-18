---
title: 'SysTime SysTime'
description: 'SysTime (BSW). BMW system time services (BAC).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW system time services (BAC).

*Repository path:* `SysTime/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (4 C file(s)) | `SysTime.c`, `SysTimeClassic.c`, `SysTime_ConcAdapter.c`, `SysTime_TimerAdapter.c` |
| `include/` (4 header(s)) | `SysTime.h`, `SysTime_AssertAdapter.h`, `SysTime_ConcAdapter.h`, `SysTime_TimerAdapter.h` |
| `autosar/` (2 ARXML) | `SysTimeClassic_paramdef.arxml`, `SysTime_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 11):

- `BUtil/PlatformTypes.h`
- `SysTime_Version.h`
- `SysTime.h`
- `SysTime_Cfg.h`
- `SysTime_TimerAdapter.h`
- `SysTime_ConcAdapter.h`
- `SysTime_AssertAdapter.h`
- `SysTime_MemMap.h`
- `SysTimeClassic_Version.h`
- `SysTimeClassic_Cfg.h`
- `Rte_SysTime.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [SysTimeClassic_IntegrationManual](../systime__systimeclassic-integrationmanual-pdf/)
- [SysTimeClassic_ReleaseNotes](../systime__systimeclassic-releasenotes-pdf/)
- [SysTimeClassic_RequirementsTable](../systime__systimeclassic-requirementstable-pdf/)
- [SysTimeGeneric_ReleaseNotes](../systime__systimegeneric-releasenotes-pdf/)
- [SysTimeGeneric_RequirementsTable](../systime__systimegeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

