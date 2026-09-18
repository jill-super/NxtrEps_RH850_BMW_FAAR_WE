---
title: 'SF041A CmplncErr'
description: 'SF041A_CmplncErr_Impl (ASW). Implementation of Compliance Error SF041A.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Compliance Error SF041A.

*Repository path:* `SF041A_CmplncErr_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CmplncErr.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `CmplncErrInit1`
- `CmplncErrPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_CmplncErr.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `CmplncErr_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CmplncErr_IntegrationManual](../sf041a_cmplncerr_impl__cmplncerr-integrationmanual-doc/)
- [CmplncErr_MDD](../sf041a_cmplncerr_impl__cmplncerr-mdd-docx/)

Source files remain in the repository next to this documentation.

