---
title: 'SF101A MotQuadDetn'
description: 'SF101A_MotQuadDetn_Impl (ASW). Implementation of Motor Quadrant Detection FDD SF101A'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Motor Quadrant Detection FDD SF101A

*Repository path:* `SF101A_MotQuadDetn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `MotQuadDetn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `MotQuadDetnInit1`
- `MotQuadDetnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_MotQuadDetn.h`
- `NxtrMath.h`
- `MotQuadDetn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotQuadDetn_IntegrationManual](../sf101a_motquaddetn_impl__motquaddetn-integrationmanual-doc/)
- [MotQuadDetn_MDD](../sf101a_motquaddetn_impl__motquaddetn-mdd-docx/)

Source files remain in the repository next to this documentation.

