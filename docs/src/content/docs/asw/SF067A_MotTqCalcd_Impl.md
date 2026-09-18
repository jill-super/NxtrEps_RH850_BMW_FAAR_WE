---
title: 'SF067A MotTqCalcd'
description: 'SF067A_MotTqCalcd_Impl (ASW). This component calculates motor torque estimate from measured Motor Currents or reference Motor Currents based on the Mo'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

This component calculates motor torque estimate from measured Motor Currents or reference Motor Currents based on the Motor Control And Thermal Protection LOA Mode

*Repository path:* `SF067A_MotTqCalcd_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotTqCalcd.c` |
| `include/` (1 header(s)) | `MotTqCalcd.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `MotTqCalcdInit1`
- `MotTqCalcdPer1`
- `MotTqCalcd_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `MotTqCalcd.h`
- `MotTqCalcd_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotTqCalcd_IntegrationManual](../sf067a_mottqcalcd_impl__mottqcalcd-integrationmanual-doc/)
- [MotTqCalcd_MDD](../sf067a_mottqcalcd_impl__mottqcalcd-mdd-docx/)

Source files remain in the repository next to this documentation.

