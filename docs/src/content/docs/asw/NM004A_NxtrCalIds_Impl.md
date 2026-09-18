---
title: 'NM004A NxtrCalIds'
description: 'NM004A_NxtrCalIds_Impl (ASW). Nexteer Calibration Identification'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Nexteer Calibration Identification

*Repository path:* `NM004A_NxtrCalIds_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 9 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `NxtrCalIds.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `NxtrCalIdsCalDevlpRd_Oper`
- `NxtrCalIdsCalRelRd_Oper`
- `NxtrCalIdsInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Rte_NxtrCalIds.h`
- `NxtrCalIds_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

