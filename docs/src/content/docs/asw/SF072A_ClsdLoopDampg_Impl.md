---
title: 'SF072A ClsdLoopDampg'
description: 'SF072A_ClsdLoopDampg_Impl (ASW). This function produces a handwheel reference torque for the closed loop system.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

This function produces a handwheel reference torque for the closed loop system.

*Repository path:* `SF072A_ClsdLoopDampg_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `ClsdLoopDampg.c` |
| `include/` (1 header(s)) | `ClsdLoopDampg.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `ClsdLoopDampgInit1`
- `ClsdLoopDampgPer1`
- `ClsdLoopDampg_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `ClsdLoopDampg.h`
- `ClsdLoopDampg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ClsdLoopDampg_IntegrationManual](../sf072a_clsdloopdampg_impl__clsdloopdampg-integrationmanual-doc/)
- [ClsdLoopDampg_MDD](../sf072a_clsdloopdampg_impl__clsdloopdampg-mdd-docx/)

Source files remain in the repository next to this documentation.

