---
title: 'ES003B PwrDiscnct'
description: 'ES003B_PwrDiscnct_Impl (CDD). Implementation of Power Disconnect FDD ES003B'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Implementation of Power Disconnect FDD ES003B

*Repository path:* `ES003B_PwrDiscnct_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `PwrDiscnct.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `PwrDiscnctInit1`
- `PwrDiscnctPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Rte_PwrDiscnct.h`
- `NxtrMath.h`
- `ElecGlbPrm.h`
- `PwrDiscnct_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [PwrDiscnct_Integration Manual](../es003b_pwrdiscnct_impl__pwrdiscnct-integration-manual-doc/)
- [PwrDiscnct_MDD](../es003b_pwrdiscnct_impl__pwrdiscnct-mdd-docx/)

Source files remain in the repository next to this documentation.

