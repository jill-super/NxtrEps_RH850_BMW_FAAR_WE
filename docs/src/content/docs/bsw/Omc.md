---
title: 'Omc Omc'
description: 'Omc (BSW). BMW Operation Mode Control (BAC).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW Operation Mode Control (BAC).

*Repository path:* `Omc/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 21 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (9 C file(s)) | `Omc.c`, `Omc_ApplAdapter.c`, `Omc_ConcAdapter.c`, `Omc_Data.c`, `Omc_ErrMemAdapter.c`, `Omc_MgmtAdapter.c`, `Omc_NvMAdapter.c`, `Omc_StdDiagAdapter.c`, `Omc_UDSAdapter.c` |
| `include/` (12 header(s)) | `Omc.h`, `OmcClassic_Version.h`, `Omc_ApplAdapter.h`, `Omc_Assert.h`, `Omc_ConcAdapter.h`, `Omc_Data.h`, `Omc_ErrMemAdapter.h`, `Omc_MgmtAdapter.h`, `Omc_NvM.h`, `Omc_NvMAdapter.h`, `Omc_StdDiagAdapter.h`, `Omc_UDSAdapter.h` |
| `autosar/` (1 ARXML) | `Omc_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Omc_Version.h`
- `Omc_Data.h`
- `Omc.h`
- `Omc_Cfg.h`
- `Omc_Assert.h`
- `Omc_ApplAdapter.h`
- `Omc_StdDiagAdapter.h`
- `Omc_ConcAdapter.h`
- `Omc_MgmtAdapter.h`
- `Omc_NvMAdapter.h`
- `Omc_UDSAdapter.h`
- `Omc_ErrMemAdapter.h`
- `BUtil/PlatformTypes.h`
- `Omc_MemMap.h`
- `OmcClassic_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [OmcClassic_IntegrationManual](../omc__omcclassic-integrationmanual-pdf/)
- [OmcClassic_ReleaseNotes](../omc__omcclassic-releasenotes-pdf/)
- [OmcClassic_UserManual](../omc__omcclassic-usermanual-pdf/)
- [OmcGeneric_ReleaseNotes](../omc__omcgeneric-releasenotes-pdf/)
- [OmcGeneric_RequirementsTable](../omc__omcgeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

