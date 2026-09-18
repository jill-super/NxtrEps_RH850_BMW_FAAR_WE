---
title: 'CM515A MotAg4Meas'
description: 'CM515A_MotAg4Meas_Impl (CDD). MotAg4Meas header file for'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

MotAg4Meas header file for

*Repository path:* `CM515A_MotAg4Meas_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 15 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_MotAg4Meas.c` |
| `include/` (1 header(s)) | `CDD_MotAg4Meas.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `MotAg4Meas_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `GetMotAg4Mecl_Oper`
- `MotAg4MeasInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_CDD_MotAg4Meas.h`
- `CDD_MotAg4Meas.h`
- `enca_regs.h`
- `CDD_MotAg4Meas_Cfg.h`
- `CDD_MotAg4Meas_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotAg4Meas_IntegrationManual](../cm515a_motag4meas_impl__motag4meas-integrationmanual-doc/)
- [MotAg4Meas_MDD](../cm515a_motag4meas_impl__motag4meas-mdd-docx/)

Source files remain in the repository next to this documentation.

