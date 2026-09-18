---
title: 'SF032A MotTqCmdSca'
description: 'SF032A_MotTqCmdSca_Impl (ASW). Implementation of Motor Torque Command Scale SF032A.'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Motor Torque Command Scale SF032A.

*Repository path:* `SF032A_MotTqCmdSca_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotTqCmdSca.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `GetMotTqCmdSca_Oper`
- `MotTqCmdScaInit1`
- `MotTqCmdScaPer1`
- `SetMotTqCmdSca_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_MotTqCmdSca.h`
- `NxtrMath.h`
- `SysGlbPrm.h`
- `MotTqCmdSca_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotTqCmdSca_IntegrationManual](../sf032a_mottqcmdsca_impl__mottqcmdsca-integrationmanual-doc/)
- [MotTqCmdSca_MDD](../sf032a_mottqcmdsca_impl__mottqcmdsca-mdd-docx/)

Source files remain in the repository next to this documentation.

