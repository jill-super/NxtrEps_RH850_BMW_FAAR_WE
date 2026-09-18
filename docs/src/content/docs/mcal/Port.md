---
title: 'Port Port'
description: 'Port (MCAL). Renesas Port driver (pin configuration).'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas Port driver (pin configuration).

*Repository path:* `Port/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* renesas: 25 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `Port.c`, `Port_Ram.c`, `Port_Version.c` |
| `include/` (7 header(s)) | `Port.h`, `Port_Debug.h`, `Port_PBTypes.h`, `Port_Ram.h`, `Port_RegWrite.h`, `Port_Types.h`, `Port_Version.h` |
| `autosar/` (6 ARXML) | `Port_bswmd_rec.arxml`, `R403_PORT_P1M_04_05.arxml`, `R403_PORT_P1M_10_11_14_15.arxml`, `R403_PORT_P1M_12_13.arxml`, `R403_PORT_P1M_18_19_22_23.arxml`, `R403_PORT_P1M_20_21.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Port_Init`
- `Port_SetPinDirection`
- `Port_SetPinDefaultDirection`
- `Port_SetPinDefaultMode`
- `Port_RefreshPortDirection`
- `Port_GetVersionInfo`
- `Port_SetPinMode`
- `Port_SetToDioMode`
- `Port_SetToAlternateMode`
- `Port_InitConfig`
- `Port_HWInitConfig`
- `Port_OpenDrainCtrlRegInit`
- `Port_DriveUnivCtrlRegInit`
- `Port_OutputLevelInvRegInit`
- `Port_FilterConfig`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 9):

- `Port.h`
- `Port_PBTypes.h`
- `Port_RegWrite.h`
- `Det.h`
- `SchM_Port.h`
- `Dem.h`
- `Port_Ram.h`
- `MemMap.h`
- `Port_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Port Integration Manual](../port__port-integration-manual-doc/)
- [R20UT3722EJ0101-AUTOSAR](../port__r20ut3722ej0101-autosar-pdf/)
- [R20UT3723EJ0101-AUTOSAR](../port__r20ut3723ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../port__r20ut3754ej0101-autosar-pdf/)

Source files remain in the repository next to this documentation.

