---
title: 'Crc Crc'
description: 'Crc (BSW). CRC calculation library.'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

CRC calculation library.

*Repository path:* `Crc/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 2 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Crc.c` |
| `include/` (1 header(s)) | `Crc.h` |
| `autosar/` (1 ARXML) | `Crc_bswmd.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 10):

- `Crc_CalculateCRC8`
- `Crc_CalculateCRC8H2F`
- `Crc_CalculateCRC16`
- `Crc_CalculateCRC32`
- `Crc_CalculateCRC32P4`
- `Crc_CalculateCRC64`
- `Crc_GetVersionInfo`
- `Crc_CalculateCRC8Runtime`
- `Crc_CalculateCRC32Runtime`
- `Crc_CalculateCRC64Runtime`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `Crc.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Crc](../crc__technicalreference-crc-pdf/)

Source files remain in the repository next to this documentation.

