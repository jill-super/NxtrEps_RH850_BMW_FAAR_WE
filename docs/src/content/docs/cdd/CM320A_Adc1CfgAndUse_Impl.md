---
title: 'CM320A Adc1CfgAndUse'
description: 'CM320A_Adc1CfgAndUse_Impl (CDD). ADC 1 Complex Driver Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

ADC 1 Complex Driver Header

*Repository path:* `CM320A_Adc1CfgAndUse_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 14 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_Adc1CfgAndUse.c` |
| `include/` (1 header(s)) | `CDD_Adc1CfgAndUse.h` |
| `autosar/` (4 ARXML) | `CDD_Adc1CfgAndUse_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 4):

- `Adc1CfgAndUseAdc1EnaCnvn_Oper`
- `Adc1CfgAndUseInit1`
- `Adc1CfgAndUsePer1`
- `Adc1CfgAndUsePer2`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_Adc1CfgAndUse.h`
- `adcd_regs.h`
- `CDD_Adc1CfgAndUse.h`
- `CDD_Adc0CfgAndUse.h`
- `CDD_Adc1CfgAndUse_Cfg.h`
- `CDD_Adc1CfgAndUse_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Adc1CfgAndUse_IntegrationManual](../cm320a_adc1cfganduse_impl__adc1cfganduse-integrationmanual-docx/)
- [Adc1CfgAndUse_MDD](../cm320a_adc1cfganduse_impl__adc1cfganduse-mdd-doc/)

Source files remain in the repository next to this documentation.

