---
title: 'CM108A DataAndAdrPar'
description: 'CM108A_DataAndAdrPar_Impl (CDD). Data and Address Parity Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Data and Address Parity Header

*Repository path:* `CM108A_DataAndAdrPar_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 11 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_DataAndAdrPar.c`, `CDD_DataAndAdrParNonRte.c` |
| `include/` (1 header(s)) | `CDD_DataAndAdrPar.h` |
| `autosar/` (2 ARXML) | `DataTypes.arxml`, `Packages.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `DataAndAdrParInit1`
- `CDD_DataAndAdrPar_Init2`
- `ChkForEcmBit28`
- `WrTestModCtrlReg`
- `InjDataParErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 11):

- `Rte_CDD_DataAndAdrPar.h`
- `CDD_DataAndAdrPar_MemMap.h`
- `CDD_DataAndAdrPar.h`
- `CDD_ExcpnHndlg.h`
- `CDD_NxtrTi.h`
- `NxtrMcuSuprtLib.h`
- `ecm_regs.h`
- `seg_regs.h`
- `dparity_regs.h`
- `csig_regs.h`
- `McuErrInj.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DataAndAdrPar Integration Manual](../cm108a_dataandadrpar_impl__dataandadrpar-integration-manual-doc/)
- [DataAndAdrPar Module Design Document](../cm108a_dataandadrpar_impl__dataandadrpar-module-design-document-docx/)

Source files remain in the repository next to this documentation.

