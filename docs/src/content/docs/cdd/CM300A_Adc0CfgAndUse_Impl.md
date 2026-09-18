---
title: 'CM300A Adc0CfgAndUse'
description: 'CM300A_Adc0CfgAndUse_Impl (CDD). ADC 0 Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

ADC 0 Complex Driver Header

*Repository path:* `CM300A_Adc0CfgAndUse_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_Adc0CfgAndUse.c`, `CDD_Adc0CfgAndUse_MotCtrl.c` |
| `include/` (2 header(s)) | `CDD_Adc0CfgAndUse.h`, `CDD_Adc0CfgAndUse_MotCtrl_MemMap.h` |
| `autosar/` (4 ARXML) | `CDD_Adc0CfgAndUse_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `Adc0CfgAndUsePer1`
- `Adc0CfgAndUseInit1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_CDD_Adc0CfgAndUse.h`
- `adcd_regs.h`
- `CDD_Adc0CfgAndUse.h`
- `CDD_Adc0CfgAndUse_Cfg.h`
- `CDD_Adc0CfgAndUse_MemMap.h`
- `CDD_MotCtrlMgr_Data.h`
- `CDD_Adc0CfgAndUse_MotCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Adc0CfgAndUse_IntegrationManual](../cm300a_adc0cfganduse_impl__adc0cfganduse-integrationmanual-docx/)
- [Adc0CfgAndUse_MDD](../cm300a_adc0cfganduse_impl__adc0cfganduse-mdd-doc/)

Source files remain in the repository next to this documentation.

