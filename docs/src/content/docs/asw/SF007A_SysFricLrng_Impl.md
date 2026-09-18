---
title: 'SF007A SysFricLrng'
description: 'SF007A_SysFricLrng_Impl (ASW). SysFricLrng Header File'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

SysFricLrng Header File

*Repository path:* `SF007A_SysFricLrng_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 15 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `SysFricLrng.c`, `SysFricLrngNonRte.c` |
| `include/` (1 header(s)) | `SysFricLrng.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `FricLrngShtDwn`
- `RunningAndCalibrationModes`
- `FricLearning`
- `RawAvrgCalc`
- `PhiCalc`
- `RangeCounterManager`
- `NTCSetReset`
- `ClearingMode`
- `ResettingMode`
- `HwAngConstraint`
- `HwVelConstraint`
- `VehSpdConstraint`
- `ColTqconstraint`
- `ClrFricLrngOperMod_Oper`
- `GetFricData_Oper`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Rte_SysFricLrng.h`
- `NxtrMath.h`
- `NxtrFixdPt.h`
- `ArchGlbPrm.h`
- `NxtrFil.h`
- `NxtrIntrpn.h`
- `SysFricLrng_MemMap.h`
- `SysFricLrng.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [SysFricLrng_IntegrationManual](../sf007a_sysfriclrng_impl__sysfriclrng-integrationmanual-doc/)
- [SysFricLrng_MDD](../sf007a_sysfriclrng_impl__sysfriclrng-mdd-docx/)

Source files remain in the repository next to this documentation.

