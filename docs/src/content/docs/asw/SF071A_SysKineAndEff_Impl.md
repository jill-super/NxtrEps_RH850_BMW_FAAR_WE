---
title: 'SF071A SysKineAndEff'
description: 'SF071A_SysKineAndEff_Impl (ASW). In a variable ratio system the kinematic ratio and mechanical efficiency of the input and motor torque can change as the'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

In a variable ratio system the kinematic ratio and mechanical efficiency of the input and motor torque can change as the rack moves.

*Repository path:* `SF071A_SysKineAndEff_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `SysKineAndEff.c` |
| `include/` (1 header(s)) | `SysKineAndEff.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `SysKineAndEffInit1`
- `SysKineAndEffPer1`
- `SysKineAndEff_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `SysKineAndEff.h`
- `SysKineAndEff_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [SysKineAndEff_IntegrationManual](../sf071a_syskineandeff_impl__syskineandeff-integrationmanual-doc/)
- [SysKineAndEff_MDD](../sf071a_syskineandeff_impl__syskineandeff-mdd-docx/)

Source files remain in the repository next to this documentation.

