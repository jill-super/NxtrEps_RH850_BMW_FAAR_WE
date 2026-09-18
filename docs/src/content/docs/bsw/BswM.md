---
title: 'BswM BswM'
description: 'BswM (BSW). Header file of MICROSAR Basic Software Mode Manager * * \details Implements AUTOSAR BswM'
---

:::tip[Origin: Vector-provided · MICROSAR]
Project-configured/generated for this ECU (DaVinci/MICROSAR tooling).
:::

## Purpose

Header file of MICROSAR Basic Software Mode Manager * * \details Implements AUTOSAR BswM

*Repository path:* `BswM/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 18 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `BswM.c` |
| `include/` (17 header(s)) | `BswM.h`, `BswM_CanSM.h`, `BswM_ComM.h`, `BswM_Dcm.h`, `BswM_EcuM.h`, `BswM_EthIf.h`, `BswM_EthSM.h`, `BswM_FrSM.h`, `BswM_J1939Dcm.h`, `BswM_J1939Nm.h`, `BswM_LinSM.h`, `BswM_LinTp.h` |
| `autosar/` (1 ARXML) | `BswM_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `BswM_InitMemory`
- `BswM_Init`
- `BswM_Deinit`
- `BswM_GetVersionInfo`
- `BswM_RequestMode`
- `BswM_RuleControl`
- `BswM_CanSM_CurrentState`
- `BswM_ComM_CurrentMode`
- `BswM_ComM_InitiateReset`
- `BswM_ComM_CurrentPNCMode`
- `BswM_Dcm_CommunicationMode_CurrentState`
- `BswM_Dcm_ApplicationUpdated`
- `BswM_EcuM_CurrentState`
- `BswM_EcuM_CurrentWakeup`
- `BswM_EcuM_RequestedState`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `BswM.h`
- `BswM_Private_Cfg.h`
- `SchM_BswM.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_BswM](../bswm__technicalreference-bswm-pdf/)

Source files remain in the repository next to this documentation.

