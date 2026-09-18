---
title: 'CM106A McuCoreCfgAndDiagc'
description: 'CM106A_McuCoreCfgAndDiagc_Impl (CDD). Mcu Core Configuration and Diagnostics Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Mcu Core Configuration and Diagnostics Complex Driver Header

*Repository path:* `CM106A_McuCoreCfgAndDiagc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_McuCoreCfgAndDiagc.c`, `CDD_McuCoreCfgAndDiagcNonRte.c` |
| `include/` (1 header(s)) | `CDD_McuCoreCfgAndDiagc.h` |
| `autosar/` (2 ARXML) | `DataTypes.arxml`, `Packages.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `McuCoreCfgAndDiagcInit1`
- `McuCoreCfgAndDiagcInit2`
- `McuCoreCfgAndDiagcInit3`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Rte_CDD_McuCoreCfgAndDiagc.h`
- `CDD_McuCoreCfgAndDiagc.h`
- `CDD_McuCoreCfgAndDiagc_MemMap.h`
- `NxtrMcuSuprtLib.h`
- `CDD_ExcpnHndlg.h`
- `sys_regs.h`
- `ecm_regs.h`
- `lockstep_regs.h`
- `McuErrInj.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [McuCoreCfgAndDiagc Integration Manual](../cm106a_mcucorecfganddiagc_impl__mcucorecfganddiagc-integration-manual-doc/)
- [McuCoreCfgAndDiagc Module Design Document](../cm106a_mcucorecfganddiagc_impl__mcucorecfganddiagc-module-design-document-docx/)

Source files remain in the repository next to this documentation.

