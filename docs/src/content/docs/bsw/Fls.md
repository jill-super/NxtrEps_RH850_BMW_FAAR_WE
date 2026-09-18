---
title: 'Fls Fls'
description: 'Fls (BSW). Renesas Flash driver (code/data flash access).'
---

:::note[Origin: Renesas-provided · MCAL]
:::

## Purpose

Renesas Flash driver (code/data flash access).

*Repository path:* `Fls/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* renesas: 31 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (6 C file(s)) | `Fls.c`, `Fls_Internal.c`, `Fls_Irq.c`, `Fls_Private_Fcu.c`, `Fls_Ram.c`, `Fls_Version.c` |
| `include/` (10 header(s)) | `Fls.h`, `Fls_Debug.h`, `Fls_Internal.h`, `Fls_Irq.h`, `Fls_PBTypes.h`, `Fls_Private_Fcu.h`, `Fls_Ram.h`, `Fls_RegWrite.h`, `Fls_Types.h`, `Fls_Version.h` |
| `autosar/` (3 ARXML) | `Fls_bswmd_rec.arxml`, `R403_FLS_P1M_04_05_10_to_15.arxml`, `R403_FLS_P1M_18_to_23.arxml` |
| Build/config | `make/*.mak`, `generate/` (DaVinci), `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Fls_Init`
- `Fls_Erase`
- `Fls_Write`
- `Fls_Read`
- `Fls_ReadImmediate`
- `Fls_Compare`
- `Fls_Cancel`
- `Fls_SetMode`
- `Fls_MainFunction`
- `Fls_GetStatus`
- `Fls_GetJobResult`
- `Fls_Suspend`
- `Fls_Resume`
- `Fls_BlankCheck`
- `Fls_GetVersionInfo`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 14):

- `Fls.h`
- `rh850_Types.h`
- `Fls_Internal.h`
- `Fls_Ram.h`
- `Dem.h`
- `Fls_RegWrite.h`
- `Fls_Private_Fcu.h`
- `Fls_Cbk.h`
- `SchM_Fls.h`
- `Det.h`
- `MemMap.h`
- `Fls_Types.h`
- `Fls_Irq.h`
- `Fls_Version.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [Fls Integration Manual](../fls__fls-integration-manual-doc/)
- [R20UT3710EJ0102-AUTOSAR](../fls__r20ut3710ej0102-autosar-pdf/)
- [R20UT3711EJ0101-AUTOSAR](../fls__r20ut3711ej0101-autosar-pdf/)
- [R20UT3754EJ0101-AUTOSAR](../fls__r20ut3754ej0101-autosar-pdf/)

Source files remain in the repository next to this documentation.

