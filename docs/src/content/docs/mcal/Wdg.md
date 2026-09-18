---
title: 'Wdg Wdg'
description: 'Wdg (MCAL). Renesas Watchdog driver.'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas Watchdog driver.

*Repository path:* `Wdg/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* renesas: 29 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (5 C file(s)) | `Wdg_59_DriverA.c`, `Wdg_59_DriverA_Irq.c`, `Wdg_59_DriverA_Private.c`, `Wdg_59_DriverA_Ram.c`, `Wdg_59_DriverA_Version.c` |
| `include/` (9 header(s)) | `Wdg_59_DriverA.h`, `Wdg_59_DriverA_Debug.h`, `Wdg_59_DriverA_Irq.h`, `Wdg_59_DriverA_PBTypes.h`, `Wdg_59_DriverA_Private.h`, `Wdg_59_DriverA_Ram.h`, `Wdg_59_DriverA_RegWrite.h`, `Wdg_59_DriverA_Types.h`, `Wdg_59_DriverA_Version.h` |
| `autosar/` (2 ARXML) | `R403_WDG_P1M_04_05_10_to_15_18_to_23.arxml`, `Wdg_bswmd_rec.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 8):

- `Wdg_59_DriverA_Init`
- `Wdg_59_DriverA_SetMode`
- `Wdg_59_DriverA_SetTriggerCondition`
- `Wdg_59_DriverA_GetVersionInfo`
- `WDG_59_DRIVERA_TRIGGERFUNCTION_ISR`
- `Wdg_59_DriverA_TriggerFunc`
- `Wdg_59_DriverA_InitDetCheck`
- `Wdg_59_DriverA_SetModeDetCheck`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Wdg_59_DriverA_PBTypes.h`
- `Det.h`
- `SchM_Wdg_59_DriverA.h`
- `Dem.h`
- `Wdg_59_DriverA_Ram.h`
- `Wdg_59_DriverA_Private.h`
- `rh850_Types.h`
- `Wdg_59_DriverA_RegWrite.h`
- `%s`
- `MemMap.h`
- `Wdg_59_DriverA_Irq.h`
- `Wdg_59_DriverA.h`
- `Wdg_59_DriverA_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [R20UT3728EJ0101-AUTOSAR](../wdg__r20ut3728ej0101-autosar-pdf/)
- [R20UT3729EJ0101-AUTOSAR](../wdg__r20ut3729ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../wdg__r20ut3754ej0101-autosar-pdf/)
- [Wdg Integration Manual](../wdg__wdg-integration-manual-doc/)

Source files remain in the repository next to this documentation.

