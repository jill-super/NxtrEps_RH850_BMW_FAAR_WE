---
title: 'SF066A EpsStEstimn'
description: 'SF066A_EpsStEstimn_Impl (ASW). Implements the SF066A FDD'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implements the SF066A FDD

*Repository path:* `SF066A_EpsStEstimn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `EpsStEstimn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `EpsStEstimnInit1`
- `EpsStEstimnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_EpsStEstimn.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `EpsStEstimn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [EpsStEstimn_IntegrationManual](../sf066a_epsstestimn_impl__epsstestimn-integrationmanual-doc/)
- [EpsStEstimn_MDD](../sf066a_epsstestimn_impl__epsstestimn-mdd-doc/)

Source files remain in the repository next to this documentation.

