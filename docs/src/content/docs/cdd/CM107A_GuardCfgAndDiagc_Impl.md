---
title: 'CM107A GuardCfgAndDiagc'
description: 'CM107A_GuardCfgAndDiagc_Impl (CDD). Declarations of global functions of CM107A Guard Configuration and Diagnostics RH850'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Declarations of global functions of CM107A Guard Configuration and Diagnostics RH850

*Repository path:* `CM107A_GuardCfgAndDiagc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 14 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_GuardCfgAndDiagc.c`, `CDD_GuardCfgAndDiagcNonRte.c` |
| `include/` (1 header(s)) | `CDD_GuardCfgAndDiagc.h` |
| `autosar/` (2 ARXML) | `DataTypes.arxml`, `Packages.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 14):

- `GuardCfgAndDiagcInit1`
- `IpgInin`
- `GuardCfgAndDiagcInit3`
- `GuardCfgAndDiagcInit2`
- `PegInin`
- `PbgInin`
- `ConfigureFilterN`
- `ChkForECMErr`
- `ChkForPBGErr`
- `Vrfy8BitPBGRegAcs`
- `Vrfy16BitPBGRegAcs`
- `Vrfy32BitPBGRegAcs`
- `InjRtPegErr`
- `InjIpgRtErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Rte_CDD_GuardCfgAndDiagc.h`
- `CDD_GuardCfgAndDiagc.h`
- `CDD_GuardCfgAndDiagc_MemMap.h`
- `CDD_ExcpnHndlg.h`
- `NxtrMcuSuprtLib.h`
- `ipg_regs.h`
- `peg_regs.h`
- `pbg_regs.h`
- `port_regs.h`
- `dnf_regs.h`
- `adcd_regs.h`
- `ecm_regs.h`
- `seg_regs.h`
- `Os.h`
- `McuErrInj.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [GuardCfgAndDiagc Integration Manual](../cm107a_guardcfganddiagc_impl__guardcfganddiagc-integration-manual-doc/)
- [GuardCfgAndDiagc Module Design Document](../cm107a_guardcfganddiagc_impl__guardcfganddiagc-module-design-document-docx/)

Source files remain in the repository next to this documentation.

