---
title: 'NM003A NxtrSwIds'
description: 'NM003A_NxtrSwIds_Impl (ASW). Nexteer Software Identifiers'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Nexteer Software Identifiers

*Repository path:* `NM003A_NxtrSwIds_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `NxtrSwIds.c` |
| `include/` (1 header(s)) | `NxtrSwIds.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `NxtrSwIds_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `generate/` (DaVinci), `tools/` |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `NxtrSwIdsInit1`
- `NxtrSwIdsPsrInfoRd_Oper`
- `NxtrSwIdsSwBuildDateTiRd_Oper`
- `NxtrSwIdsSwRelInfoRd_Oper`
- `NxtrSwIdsSwRelNrRd_Oper`
- `NxtrSwIdsSwRelVerRd_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_NxtrSwIds.h`
- `NxtrSwIds.h`
- `NxtrSwIds_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

