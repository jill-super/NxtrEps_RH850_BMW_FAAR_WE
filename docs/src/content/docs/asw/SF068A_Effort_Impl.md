---
title: 'SF068A Effort'
description: 'SF068A_Effort_Impl (ASW). This function produces a handwheel reference torque for the closed loop system.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

This function produces a handwheel reference torque for the closed loop system.

*Repository path:* `SF068A_Effort_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Effort.c` |
| `include/` (1 header(s)) | `Effort.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `EffortInit1`
- `EffortPer1`
- `Effort_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Effort.h`
- `Effort_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Effort_IntegrationManual](../sf068a_effort_impl__effort-integrationmanual-doc/)
- [Effort_MDD](../sf068a_effort_impl__effort-mdd-docx/)

Source files remain in the repository next to this documentation.

