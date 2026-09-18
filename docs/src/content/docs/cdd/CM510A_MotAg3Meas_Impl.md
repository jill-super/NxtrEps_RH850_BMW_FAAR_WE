---
title: 'CM510A MotAg3Meas'
description: 'CM510A_MotAg3Meas_Impl (CDD). MotAg3Meas header file for'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

MotAg3Meas header file for

*Repository path:* `CM510A_MotAg3Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 15 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_MotAg3Meas.c` |
| `include/` (1 header(s)) | `CDD_MotAg3Meas.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `MotAg3Meas_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `GetMotAg3Mecl_Oper`
- `MotAg3MeasInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_CDD_MotAg3Meas.h`
- `CDD_MotAg3Meas.h`
- `enca_regs.h`
- `CDD_MotAg3Meas_Cfg.h`
- `CDD_MotAg3Meas_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAg3Meas_IntegrationManual](../cm510a_motag3meas_impl__motag3meas-integrationmanual-doc/)
- [MotAg3Meas_MDD](../cm510a_motag3meas_impl__motag3meas-mdd-docx/)

Source files remain in the repository next to this documentation.

