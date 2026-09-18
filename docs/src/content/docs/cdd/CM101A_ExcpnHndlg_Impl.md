---
title: 'CM101A ExcpnHndlg'
description: 'CM101A_ExcpnHndlg_Impl (CDD). Declarations of McuDiagc1 data type and global functions of CM101A Exception Handling RH850'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Declarations of McuDiagc1 data type and global functions of CM101A Exception Handling RH850

*Repository path:* `CM101A_ExcpnHndlg_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 17 file(s), renesas: 1 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `CDD_ExcpnHndlg.c`, `CDD_ExcpnHndlgIrq.c`, `CDD_ExcpnHndlgNonRte.c` |
| `include/` (2 header(s)) | `CDD_ExcpnHndlg.h`, `CDD_ExcpnHndlg_private.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `ExcpnHndlg_bswmd.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `SetMcuDiagcIdnData`
- `GetMcuDiagcIdnData`
- `SysErrIrq`
- `FpuErrIrq`
- `AlgnErrIrq`
- `ResdOperIrq`
- `ExcpnHndlgInit1`
- `FeNmiPeg`
- `FeNmiDmaTrf`
- `FeNmiDmaRegAcsProtnErr`
- `FeNmiEcmMstChkrCmp`
- `FeNmiWdg`
- `ProcUkwnExcpnErr`
- `ProcMpuExcpnErr`
- `ProcPrvlgdInstrExcpnErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Rte_CDD_ExcpnHndlg.h`
- `CDD_ExcpnHndlg.h`
- `CDD_ExcpnHndlg_private.h`
- `sys_regs.h`
- `ram_regs.h`
- `ecm_regs.h`
- `MemMap.h`
- `CDD_ExcpnHndlg_MemMap.h`
- `seg_regs.h`
- `ecc_regs.h`
- `NxtrMcuSuprtLib.h`
- `dma_regs.h`
- `CDD_ExcpnHndlg_Cfg.h`
- `WdgM.h`
- `WdgM_PBcfg.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [ExcpnHndlg Integration Manual](../cm101a_excpnhndlg_impl__excpnhndlg-integration-manual-doc/)
- [ExcpnHndlg Module Design Document](../cm101a_excpnhndlg_impl__excpnhndlg-module-design-document-docx/)

Source files remain in the repository next to this documentation.

