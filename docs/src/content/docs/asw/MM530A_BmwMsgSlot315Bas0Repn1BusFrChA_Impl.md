---
title: 'MM530A BmwMsgSlot315Bas0Repn1BusFrChA'
description: 'MM530A_BmwMsgSlot315Bas0Repn1BusFrChA_Impl (ASW). BMW Message Slot 315 Base 0 Repetition 1 Bus FlexRay Channel A Processing (MM530A)'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

BMW Message Slot 315 Base 0 Repetition 1 Bus FlexRay Channel A Processing (MM530A)

*Repository path:* `MM530A_BmwMsgSlot315Bas0Repn1BusFrChA_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 10 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwMsgSlot315Bas0Repn1BusFrChA.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `BmwMsgSlot315Bas0Repn1BusFrChA_Init1`
- `BmwMsgSlot315Bas0Repn1BusFrChA_Per1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_BmwMsgSlot315Bas0Repn1BusFrChA.h`
- `NxtrMath.h`
- `BmwMsgSlot315Bas0Repn1BusFrChA_MemMap.h`

## Documents

No Word/PDF documents were found for this module.

