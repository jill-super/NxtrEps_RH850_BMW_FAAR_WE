---
title: 'AR099A McalErrHndlg'
description: 'AR099A_McalErrHndlg_Impl (MCAL). MCAL Error Handling'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

MCAL Error Handling

*Repository path:* `AR099A_McalErrHndlg_Impl/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 19 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `McalErrHndlg.c`, `McalErrHndlgNonRte.c` |
| `include/` (1 header(s)) | `McalErrHndlg.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 5):

- `HndlMcalDemErr`
- `HndlMcalWrVrfyErr`
- `Fls_CallSwitchBFlashErrorNotification`
- `McalErrHndlgInit1`
- `McalErrHndlgPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 15):

- `Rte_McalErrHndlg.h`
- `McalErrHndlg_MemMap.h`
- `Std_Types.h`
- `Mcu.h`
- `Mcu_Reg.h`
- `Mcu_Cfg.h`
- `Mcu_PBTypes.h`
- `Fls_Cfg.h`
- `Spi_Cfg.h`
- `Dem.h`
- `ram_regs.h`
- `CDD_ExcpnHndlg.h`
- `McalErrHndlg.h`
- `sys_regs.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [McalErrHndlg_IntegrationManual](../ar099a_mcalerrhndlg_impl__mcalerrhndlg-integrationmanual-docx/)

Source files remain in the repository next to this documentation.

