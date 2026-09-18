---
title: 'StdDiag StdDiag'
description: 'StdDiag (BSW). BMW standard diagnostics helpers (BAC session handling).'
---

:::note[Origin: BMW-provided · BAC (BMW AUTOSAR Core)]
:::

## Purpose

BMW standard diagnostics helpers (BAC session handling).

*Repository path:* `StdDiag/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* bmw: 32 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (17 C file(s)) | `StdDiag.c`, `StdDiagClassic.c`, `StdDiag_ActiveSessionState.c`, `StdDiag_Adt.c`, `StdDiag_AdtUploadDownload.c`, `StdDiag_AppAdapter.c`, `StdDiag_CheckProgPrecondition.c`, `StdDiag_DarhAdapter.c`, `StdDiag_Dlt.c`, `StdDiag_ErrMemAdapter.c`, `StdDiag_IDRL.c`, `StdDiag_IDRLAdapter.c` |
| `include/` (15 header(s)) | `StdDiag.h`, `StdDiag_AdtInternal.h`, `StdDiag_AdtTypes.h`, `StdDiag_AppAdapter.h`, `StdDiag_AssertAdapter.h`, `StdDiag_DarhAdapter.h`, `StdDiag_DcmTypes.h`, `StdDiag_ErrMemAdapter.h`, `StdDiag_IDRLAdapter.h`, `StdDiag_Internal.h`, `StdDiag_MgmtAdapter.h`, `StdDiag_OmcAdapter.h` |
| `autosar/` (2 ARXML) | `StdDiagClassic_paramdef.arxml`, `StdDiag_paramdef.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `BUtil/PlatformTypes.h`
- `StdDiag_Version.h`
- `StdDiag.h`
- `StdDiag_Internal.h`
- `StdDiag_ProgPreparation.h`
- `StdDiag_AssertAdapter.h`
- `StdDiag_MemMap.h`
- `StdDiagClassic_Cfg.h`
- `StdDiagClassic_PBCfg.h`
- `StdDiagClassic_Version.h`
- `Rte_StdDiag.h`
- `StdDiag_UDSAdapter.h`
- `StdDiag_OmcAdapter.h`
- `StdDiag_DarhAdapter.h`
- `StdDiag_Cfg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [StdDiagClassic_IntegrationManual](../stddiag__stddiagclassic-integrationmanual-pdf/)
- [StdDiagClassic_ReleaseNotes](../stddiag__stddiagclassic-releasenotes-pdf/)
- [StdDiagClassic_RequirementsTable](../stddiag__stddiagclassic-requirementstable-pdf/)
- [StdDiagGeneric_ReleaseNotes](../stddiag__stddiaggeneric-releasenotes-pdf/)
- [StdDiagGeneric_RequirementsTable](../stddiag__stddiaggeneric-requirementstable-pdf/)

Source files remain in the repository next to this documentation.

