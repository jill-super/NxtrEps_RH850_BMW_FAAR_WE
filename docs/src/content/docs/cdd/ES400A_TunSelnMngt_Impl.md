---
title: 'ES400A TunSelnMngt'
description: 'ES400A_TunSelnMngt_Impl (CDD). Header file for Tuning Selection Management'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Header file for Tuning Selection Management

*Repository path:* `ES400A_TunSelnMngt_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 18 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `TunSelnMngt.c`, `TunSelnMngt_private.c` |
| `include/` (1 header(s)) | `TunSelnMngt.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml`, `TunSelnMngt_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 13):

- `SwtCalIdx`
- `IdxChgMngt`
- `MemCopy32Bit`
- `MemCopy8Bit`
- `SegModAdrInfo`
- `SegModStdInfo`
- `SegModAdrMpg`
- `CopyCalPageReq_Oper`
- `GetCalPageReq_Oper`
- `GetSegInfoReq_Oper`
- `OnlineTunRamAdrMpg_Oper`
- `SetCalPageReq_Oper`
- `TunSelnMngtInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `Rte_TunSelnMngt.h`
- `TunSelnMngt_Cfg_private.h`
- `TunSelnMngt_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ES400A_TunSelnMngt_Integration_Manual](../es400a_tunselnmngt_impl__es400a-tunselnmngt-integration-manual-doc/)
- [ES400A_TunSelnMngt_MDD](../es400a_tunselnmngt_impl__es400a-tunselnmngt-mdd-docx/)

Source files remain in the repository next to this documentation.

