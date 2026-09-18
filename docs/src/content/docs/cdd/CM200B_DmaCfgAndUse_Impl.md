---
title: 'CM200B DmaCfgAndUse'
description: 'CM200B_DmaCfgAndUse_Impl (CDD). DMA Configuration and Use header file'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

DMA Configuration and Use header file

*Repository path:* `CM200B_DmaCfgAndUse_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 19 file(s), renesas: 1 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_DmaCfgAndUse.c` |
| `include/` (2 header(s)) | `CDD_DmaCfgAndUse.h`, `NxtrDmaRegs.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 8):

- `DmaRegInin`
- `DmaCfgAndUseInit1`
- `DmaCfgAndUsePer1`
- `DmaEna2MilliSecToMotCtrlTrf_Oper`
- `DmaWaitForMotCtrlTo2MilliSecTrf_Oper`
- `MotAg0SnsrCfgDmaStrt_Oper`
- `InjDmaErr`
- `InjMcuDiagcErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Rte_CDD_DmaCfgAndUse.h`
- `CDD_DmaCfgAndUse.h`
- `NxtrDmaRegs.h`
- `NxtrMath.h`
- `csih_regs.h`
- `adcd_regs.h`
- `tsg3_regs.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_MotAg0Meas.h`
- `CDD_MotAg1Meas.h`
- `Os.h`
- `McuErrInj.h`
- `CDD_DmaCfgAndUse_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DmaCfgAndUse_Integration_Manual](../cm200b_dmacfganduse_impl__dmacfganduse-integration-manual-doc/)
- [DmaCfgAndUse_MDD](../cm200b_dmacfganduse_impl__dmacfganduse-mdd-docx/)

Source files remain in the repository next to this documentation.

