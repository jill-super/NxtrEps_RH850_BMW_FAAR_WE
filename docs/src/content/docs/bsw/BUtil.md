---
title: 'BUtil BUtil'
description: 'BUtil (BSW). BMW utility library (BAC).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW utility library (BAC).

*Repository path:* `BUtil/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 18 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `BUtil_AddressFormat.c`, `BUtil_Math.c`, `BUtil_UDSAdapterHelper.c` |
| `include/` (10 header(s)) | `BUtilClassic_Version.h`, `BUtil_AddressFormat.h`, `BUtil_Algorithm.h`, `BUtil_Assert.h`, `BUtil_BitArray.h`, `BUtil_ByteMask.h`, `BUtil_Math.h`, `BUtil_Types.h`, `BUtil_UDSAdapterHelper.h`, `BUtil_Version.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `BUtil_AddressFormat.h`
- `BUtil_ByteMask.h`
- `BUtil_BitArray.h`
- `BUtil_Version.h`
- `BUtil_MemMap.h`
- `BUtil_Math.h`
- `BUtil_UDSAdapterHelper.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BUtilClassic_IntegrationManual](../butil__butilclassic-integrationmanual-pdf/)
- [BUtilClassic_ReleaseNotes](../butil__butilclassic-releasenotes-pdf/)
- [BUtilClassic_UserManual](../butil__butilclassic-usermanual-pdf/)
- [BUtilGeneric_ReleaseNotes](../butil__butilgeneric-releasenotes-pdf/)

Source files remain in the repository next to this documentation.

