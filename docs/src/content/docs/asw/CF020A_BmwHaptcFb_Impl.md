---
title: 'CF020A BmwHaptcFb'
description: 'CF020A_BmwHaptcFb_Impl (ASW). CF020A Implementation - Bmw Haptic Feedback'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

CF020A Implementation - Bmw Haptic Feedback

*Repository path:* `CF020A_BmwHaptcFb_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BmwHaptcFb.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `CalcBmwHaptcFbPatNr`
- `CalcBmwHaptcFbIntenNr`
- `CalcHwOscnEna`
- `CalcAmpAndFrq`
- `BmwHaptcFbInit1`
- `BmwHaptcFbPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `Rte_BmwHaptcFb.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `BmwHaptcFb_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [BmwHaptcFb_IntegrationManual](../cf020a_bmwhaptcfb_impl__bmwhaptcfb-integrationmanual-doc/)
- [BmwHaptcFb_MDD](../cf020a_bmwhaptcfb_impl__bmwhaptcfb-mdd-docx/)

Source files remain in the repository next to this documentation.

