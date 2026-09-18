---
title: 'Mcu Mcu'
description: 'Mcu (MCAL). Renesas RH850 P1x MCU driver (clock, reset, power modes).'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas RH850 P1x MCU driver (clock, reset, power modes).

*Repository path:* `Mcu/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 1 file(s), renesas: 28 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (5 C file(s)) | `Mcu.c`, `Mcu_Irq.c`, `Mcu_Ram.c`, `Mcu_Version.c`, `NxtrMcuIrqPatch.c` |
| `include/` (8 header(s)) | `Mcu.h`, `Mcu_Debug.h`, `Mcu_Irq.h`, `Mcu_PBTypes.h`, `Mcu_Ram.h`, `Mcu_RegWrite.h`, `Mcu_Types.h`, `Mcu_Version.h` |
| `autosar/` (3 ARXML) | `Mcu_bswmd_rec.arxml`, `R403_MCU_P1M_04_05.arxml`, `R403_MCU_P1M_10_to_15_18_to_23.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `MCU_RESET_CALLOUT`
- `Mcu_Init`
- `Mcu_InitRamSection`
- `Mcu_InitClock`
- `Mcu_DistributePllClock`
- `Mcu_GetPllStatus`
- `Mcu_GetResetReason`
- `Mcu_GetResetRawValue`
- `Mcu_PerformReset`
- `Mcu_SetMode`
- `Mcu_GetRamState`
- `Mcu_GetVersionInfo`
- `Mcu_EcmReleaseErrorOutPin`
- `MCU_FEINT_ISR`
- `MCU_ECM_EIC_ISR`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 12):

- `Mcu_PBTypes.h`
- `Mcu_Ram.h`
- `Det.h`
- `Dem.h`
- `SchM_Mcu.h`
- `Mcu_Reg.h`
- `Mcu.h`
- `Mcu_Cbk.h`
- `Mcu_RegWrite.h`
- `MemMap.h`
- `Mcu_Irq.h`
- `Mcu_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Mcu Integration Manual](../mcu__mcu-integration-manual-doc/)
- [R20UT3720EJ0101-AUTOSAR](../mcu__r20ut3720ej0101-autosar-pdf/)
- [R20UT3721EJ0101-AUTOSAR](../mcu__r20ut3721ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../mcu__r20ut3754ej0101-autosar-pdf/)

Source files remain in the repository next to this documentation.

