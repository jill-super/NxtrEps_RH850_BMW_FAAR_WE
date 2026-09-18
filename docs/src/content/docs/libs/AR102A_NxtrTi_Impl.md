---
title: 'AR102A NxtrTi'
description: 'AR102A_NxtrTi_Impl (LIBS). Nexteer Time Library Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Nexteer Time Library Complex Driver Header

*Repository path:* `AR102A_NxtrTi_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_NxtrTi.c`, `CDD_NxtrTi_Init.c` |
| `include/` (1 header(s)) | `CDD_NxtrTi.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `NxtrTiInit0`
- `GetRefTmr100MicroSec32bit_Oper`
- `GetRefTmr1MicroSec32bit_Oper`
- `GetTiSpan100MicroSec32bit_Oper`
- `GetTiSpan1MicroSec32bit_Oper`
- `NxtrTiInit1`
- `NxtrTiPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_NxtrTi.h`
- `CDD_NxtrTi.h`
- `tauj_regs.h`
- `NxtrMath.h`
- `McuErrInj.h`
- `CDD_NxtrTi_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CDD_NxtrTi_MDD](../ar102a_nxtrti_impl__cdd-nxtrti-mdd-docx/)
- [NxtrTi Integration Manual](../ar102a_nxtrti_impl__nxtrti-integration-manual-doc/)

Source files remain in the repository next to this documentation.

