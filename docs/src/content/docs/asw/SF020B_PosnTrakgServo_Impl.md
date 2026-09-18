---
title: 'SF020B PosnTrakgServo'
description: 'SF020B_PosnTrakgServo_Impl (ASW). Implementation of Position Tracking Servo (FDD SF020B)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Position Tracking Servo (FDD SF020B)

*Repository path:* `SF020B_PosnTrakgServo_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PosnTrakgServo.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `SVReset`
- `PosnTrakgServoInit1`
- `PosnTrakgServoPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_PosnTrakgServo.h`
- `NxtrMath.h`
- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `SysGlbPrm.h`
- `ArchGlbPrm.h`
- `PosnTrakgServo_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PosnTrakgServo_IntegrationManual](../sf020b_posntrakgservo_impl__posntrakgservo-integrationmanual-doc/)
- [PosnTrakgServo_MDD](../sf020b_posntrakgservo_impl__posntrakgservo-mdd-docx/)

Source files remain in the repository next to this documentation.

