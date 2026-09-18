---
title: 'CM104A EcmOutpAndDiagc'
description: 'CM104A_EcmOutpAndDiagc_Impl (CDD). Error Control Module Output and Diagnostics Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Error Control Module Output and Diagnostics Complex Driver Header

*Repository path:* `CM104A_EcmOutpAndDiagc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 14 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_EcmOutpAndDiagc.c`, `CDD_EcmOutpAndDiagcNonRte.c` |
| `include/` (1 header(s)) | `CDD_EcmOutpAndDiagc.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `CtrlErrOut_Oper`
- `EcmOutpAndDiagcInit1`
- `EcmOutpAndDiagcInit3`
- `EcmOutpAndDiagcInit4`
- `EcmOutpAndDiagcInit2`
- `InjEcmMstChkrRtErr`
- `InjUkwnStrtUpDetdErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 10):

- `Rte_CDD_EcmOutpAndDiagc.h`
- `CDD_EcmOutpAndDiagc.h`
- `ecm_regs.h`
- `NxtrMcuSuprtLib.h`
- `CDD_EcmOutpAndDiagc_MemMap.h`
- `Os.h`
- `CDD_ExcpnHndlg.h`
- `intc_regs.h`
- `Std_Types.h`
- `McuErrInj.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [EcmOutpAndDiagc Integration Manual](../cm104a_ecmoutpanddiagc_impl__ecmoutpanddiagc-integration-manual-doc/)
- [EcmOutpAndDiagc Module Design Document](../cm104a_ecmoutpanddiagc_impl__ecmoutpanddiagc-module-design-document-docx/)

Source files remain in the repository next to this documentation.

