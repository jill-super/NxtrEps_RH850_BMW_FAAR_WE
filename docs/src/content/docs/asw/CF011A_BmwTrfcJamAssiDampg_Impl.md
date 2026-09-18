---
title: 'CF011A BmwTrfcJamAssiDampg'
description: 'CF011A_BmwTrfcJamAssiDampg_Impl (ASW). The BMW Traffic Jam Assist Damping'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

The BMW Traffic Jam Assist Damping

*Repository path:* `CF011A_BmwTrfcJamAssiDampg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwTrfcJamAssiDampg.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `CalcnTrfcJamAssiSt`
- `ProcessBmwTrfcJamAssiDampgErr`
- `BmwTrfcJamAssiDampgInit1`
- `BmwTrfcJamAssiDampgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_BmwTrfcJamAssiDampg.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `SysGlbPrm.h`
- `BmwTrfcJamAssiDampg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwTrfcJamAssiDampg_IntegrationManual](../cf011a_bmwtrfcjamassidampg_impl__bmwtrfcjamassidampg-integrationmanual-doc/)
- [BmwTrfcJamAssiDampg_MDD](../cf011a_bmwtrfcjamassidampg_impl__bmwtrfcjamassidampg-mdd-docx/)

Source files remain in the repository next to this documentation.

