---
title: 'Coding Coding'
description: 'Coding (BSW). BMW variant coding module (BAC).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW variant coding module (BAC).

*Repository path:* `Coding/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 23 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (11 C file(s)) | `Coding.c`, `Coding_ConcAdapter.c`, `Coding_CryptoAdapter.c`, `Coding_Data.c`, `Coding_DlogAdapter.c`, `Coding_ErrMemAdapter.c`, `Coding_MgmtAdapter.c`, `Coding_NvMAdapter.c`, `Coding_TimerAdapter.c`, `Coding_UDSAdapter.c`, `Coding_VinAdapter.c` |
| `include/` (12 header(s)) | `Coding.h`, `Coding_ApplAdapter.h`, `Coding_Assert.h`, `Coding_ConcAdapter.h`, `Coding_CryptoAdapter.h`, `Coding_Data.h`, `Coding_DlogAdapter.h`, `Coding_ErrMemAdapter.h`, `Coding_MgmtAdapter.h`, `Coding_NvMAdapter.h`, `Coding_TimerAdapter.h`, `Coding_UDSAdapter.h` |
| `autosar/` (2 ARXML) | `CodingClassic_paramdef.arxml`, `Coding_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Coding.h`
- `BUtil/PlatformTypes.h`
- `BUtil/GenericErrMemTypes.h`
- `BUtil/GenericNvMTypes.h`
- `BUtil_ByteMask.h`
- `Coding_TimerAdapter.h`
- `Coding_DlogAdapter.h`
- `Coding_ConcAdapter.h`
- `Coding_Assert.h`
- `Coding_CryptoAdapter.h`
- `Coding_MgmtAdapter.h`
- `Coding_ErrMemAdapter.h`
- `Coding_NvMAdapter.h`
- `Coding_UDSAdapter.h`
- `Coding_ApplAdapter.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CodingClassic_IntegrationManual](../coding__codingclassic-integrationmanual-pdf/)
- [CodingClassic_ReleaseNotes](../coding__codingclassic-releasenotes-pdf/)
- [CodingClassic_RequirementsTable](../coding__codingclassic-requirementstable-pdf/)
- [CodingGeneric_ReleaseNotes](../coding__codinggeneric-releasenotes-pdf/)
- [CodingGeneric_RequirementsTable](../coding__codinggeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

