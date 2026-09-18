---
title: 'DF003A McuErrInj'
description: 'DF003A_McuErrInj_Impl (CDD). Micro Diag Error Injection header file'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Micro Diag Error Injection header file

*Repository path:* `DF003A_McuErrInj_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `McuErrInj.c` |
| `include/` (2 header(s)) | `McuErrInj.h`, `McuErrInjNonRte_MemMap.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `ClrErrInjReg_Oper`
- `ReadErrInjReg_Oper`
- `StrtErrInjCntr_Oper`
- `UpdErrInjReg_Oper`
- `McuDiagcTestTrustd`
- `InjVrfyCritRegErr`
- `InjMcuVltgMonrErr`
- `InjClkMonrErr`
- `InjOsTmpGenericRtErr`
- `InjOsPrmntGenericRtErr`
- `InjWdgErr`
- `InjFpuErr`
- `InjMemProtnErr`
- `InjModErr`
- `InjMcuRtErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_McuErrInj.h`
- `ram_regs.h`
- `Os.h`
- `McuErrInj.h`
- `McuErrInjNonRte_MemMap.h`
- `McuErrInj_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [McuErrInj Integration Manual](../df003a_mcuerrinj_impl__mcuerrinj-integration-manual-docx/)
- [McuErrInj Module Design Document](../df003a_mcuerrinj_impl__mcuerrinj-module-design-document-doc/)

Source files remain in the repository next to this documentation.

