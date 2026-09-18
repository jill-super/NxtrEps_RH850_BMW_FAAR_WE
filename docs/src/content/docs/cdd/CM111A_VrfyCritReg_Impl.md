---
title: 'CM111A VrfyCritReg'
description: 'CM111A_VrfyCritReg_Impl (CDD). Critical Register Verification header file'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Critical Register Verification header file

*Repository path:* `CM111A_VrfyCritReg_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 14 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `CDD_VrfyCritReg.c` |
| `include/` (1 header(s)) | `CDD_VrfyCritReg.h` |
| `autosar/` (4 ARXML) | `CDD_VrfyCritReg_bswmd.arxml`, `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 7):

- `CritRegPerChk`
- `CritRegInitChk`
- `MCalReadVrfyFailFltInfo_Oper`
- `VrfyCritRegInit1`
- `VrfyCritRegPer1`
- `VrfyCritRegPer2`
- `InjVrfyCritRegErr`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_CDD_VrfyCritReg.h`
- `CDD_VrfyCritReg.h`
- `Os.h`
- `CDD_VrfyCritReg_Cfg_private.h`
- `McuErrInj.h`
- `CDD_VrfyCritReg_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [VrfyCritReg_IntegrationManual](../cm111a_vrfycritreg_impl__vrfycritreg-integrationmanual-doc/)
- [VrfyCritReg_MDD](../cm111a_vrfycritreg_impl__vrfycritreg-mdd-docx/)

Source files remain in the repository next to this documentation.

