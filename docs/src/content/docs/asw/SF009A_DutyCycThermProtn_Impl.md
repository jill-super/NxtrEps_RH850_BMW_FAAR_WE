---
title: 'SF009A DutyCycThermProtn'
description: 'SF009A_DutyCycThermProtn_Impl (ASW). The purpose of the Thermal Duty Cycle Protection is to limit and protect the system from excessive use,'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

The purpose of the Thermal Duty Cycle Protection is to limit and protect the system from excessive use,

*Repository path:* `SF009A_DutyCycThermProtn_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 12 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `DutyCycThermProtn.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 11):

- `FiltSVReinit`
- `TemperatureSelection`
- `TemperatureLimiting`
- `MultiFilterPercMax`
- `ThermalLoadLimit`
- `DecoderandSubsystem`
- `TherrmalLimitScaling`
- `ThermalLimitStatus`
- `UseInpLowr`
- `DutyCycThermProtnInit1`
- `DutyCycThermProtnPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_DutyCycThermProtn.h`
- `NxtrIntrpn.h`
- `NxtrFil.h`
- `NxtrMath.h`
- `ArchGlbPrm.h`
- `SysGlbPrm.h`
- `NxtrFixdPt.h`
- `DutyCycThermProtn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [DutyCycThermProtn_Integration Manual](../sf009a_dutycycthermprotn_impl__dutycycthermprotn-integration-manual-doc/)
- [DutyCycThermProtn_MDD](../sf009a_dutycycthermprotn_impl__dutycycthermprotn-mdd-docx/)

Source files remain in the repository next to this documentation.

