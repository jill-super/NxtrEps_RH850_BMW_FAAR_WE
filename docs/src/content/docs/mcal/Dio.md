---
title: 'Dio Dio'
description: 'Dio (MCAL). Renesas Digital I/O driver.'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas Digital I/O driver.

*Repository path:* `Dio/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* renesas: 24 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (3 C file(s)) | `Dio.c`, `Dio_Ram.c`, `Dio_Version.c` |
| `include/` (6 header(s)) | `Dio.h`, `Dio_Debug.h`, `Dio_PBTypes.h`, `Dio_Ram.h`, `Dio_RegWrite.h`, `Dio_Version.h` |
| `autosar/` (3 ARXML) | `Dio_bswmd_rec.arxml`, `R403_DIO_P1M_04_05_12_13_20_21.arxml`, `R403_DIO_P1M_10_11_14_15_18_19_22_23.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `Dio_ReadPort`
- `Dio_WritePort`
- `Dio_ReadChannel`
- `Dio_WriteChannel`
- `Dio_MaskedWritePort`
- `Dio_ReadChannelGroup`
- `Dio_WriteChannelGroup`
- `Dio_Init`
- `Dio_FlipChannel`
- `Dio_GetVersionInfo`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 8):

- `Dio.h`
- `Dio_RegWrite.h`
- `Dio_Ram.h`
- `Det.h`
- `SchM_Dio.h`
- `MemMap.h`
- `Dio_PBTypes.h`
- `Dio_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Dio Integration Manual](../dio__dio-integration-manual-doc/)
- [R20UT3708EJ0101-AUTOSAR](../dio__r20ut3708ej0101-autosar-pdf/)
- [R20UT3709EJ0101-AUTOSAR](../dio__r20ut3709ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../dio__r20ut3754ej0101-autosar-pdf/)

Source files remain in the repository next to this documentation.

