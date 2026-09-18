---
title: 'CM112A CoreVltgMonr'
description: 'CM112A_CoreVltgMonr_Impl (CDD). Core Voltage Monitor Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Core Voltage Monitor Complex Driver Header

*Repository path:* `CM112A_CoreVltgMonr_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_CoreVltgMonr.c`, `CDD_CoreVltgMonrNonRte.c` |
| `include/` (1 header(s)) | `CDD_CoreVltgMonr.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `CoreVltgMonrInit1`
- `CoreVltgMonrInit2`
- `Dly12MicroSec`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_CoreVltgMonr.h`
- `CDD_CoreVltgMonr_MemMap.h`
- `CDD_CoreVltgMonr.h`
- `NxtrMcuSuprtLib.h`
- `sys_regs.h`
- `CDD_ExcpnHndlg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CoreVltgMonr_IntegrationManual](../cm112a_corevltgmonr_impl__corevltgmonr-integrationmanual-doc/)
- [CoreVltgMonr_MDD](../cm112a_corevltgmonr_impl__corevltgmonr-mdd-docx/)

Source files remain in the repository next to this documentation.

