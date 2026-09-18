---
title: 'Spi Spi'
description: 'Spi (MCAL). Renesas SPI handler/driver (serial peripheral interface).'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas SPI handler/driver (serial peripheral interface).

*Repository path:* `Spi/` · *AUTOSAR layer:* [Microcontroller Abstraction (MCAL)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* renesas: 31 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (6 C file(s)) | `Spi.c`, `Spi_Driver.c`, `Spi_Irq.c`, `Spi_Ram.c`, `Spi_Scheduler.c`, `Spi_Version.c` |
| `include/` (10 header(s)) | `Spi.h`, `Spi_Driver.h`, `Spi_Irq.h`, `Spi_LTTypes.h`, `Spi_PBTypes.h`, `Spi_Ram.h`, `Spi_RegWrite.h`, `Spi_Scheduler.h`, `Spi_Types.h`, `Spi_Version.h` |
| `autosar/` (3 ARXML) | `R403_SPI_P1M_04_05_12_13_20_21.arxml`, `R403_SPI_P1M_10_11_14_15_18_19_22_23.arxml`, `Spi_bswmd_rec.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Spi_Init`
- `Spi_DeInit`
- `Spi_WriteIB`
- `Spi_AsyncTransmit`
- `Spi_ReadIB`
- `Spi_SetupEB`
- `Spi_GetStatus`
- `Spi_GetJobResult`
- `Spi_GetSequenceResult`
- `Spi_GetVersionInfo`
- `Spi_SyncTransmit`
- `Spi_GetHWUnitStatus`
- `Spi_Cancel`
- `Spi_SetAsyncMode`
- `Spi_MainFunction_Handling`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 13):

- `Spi.h`
- `Spi_Scheduler.h`
- `Spi_Ram.h`
- `Spi_Driver.h`
- `Dem.h`
- `Det.h`
- `U:/temp/MemMap.h`
- `MemMap.h`
- `rh850_Types.h`
- `Spi_RegWrite.h`
- `Spi_Irq.h`
- `Spi_PBTypes.h`
- `Spi_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [R20UT3726EJ0101-AUTOSAR](../spi__r20ut3726ej0101-autosar-pdf/)
- [R20UT3727EJ0101-AUTOSAR](../spi__r20ut3727ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../spi__r20ut3754ej0101-autosar-pdf/)
- [Spi Integration Manual](../spi__spi-integration-manual-doc/)

Source files remain in the repository next to this documentation.

