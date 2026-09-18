---
title: 'ES999A ElecGlbPrm'
description: 'ES999A_ElecGlbPrm_Impl (CDD). Electrical global parameter definitions'
---

:::tip[Origin: Custom · Nexteer in-house]
:::

## Purpose

Electrical global parameter definitions

*Repository path:* `ES999A_ElecGlbPrm_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 6 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `ElecGlbPrm.c` |
| `include/` (2 header(s)) | `ElecGlbPrm.h`, `ElecGlbPrm_MemMap.h` |
| `autosar/` (1 ARXML) | `ElecGlbPrm_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

No `FUNC(...)` AUTOSAR-style entry points were detected in the scanned headers (the module may expose RTE ports, generated interfaces, or data tables instead). See the key files above and the design documents below.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Std_Types.h`
- `ElecGlbPrm.h`
- `ElecGlbPrm_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ElecGlbPrm_IntegrationManual](../es999a_elecglbprm_impl__elecglbprm-integrationmanual-doc/)
- [ElecGlbPrm_MDD](../es999a_elecglbprm_impl__elecglbprm-mdd-docx/)

Source files remain in the repository next to this documentation.

