---
title: 'CM800A SyncCrc'
description: 'CM800A_SyncCrc_Impl (CDD). Header file for the CM800A SyncCRC component'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Header file for the CM800A SyncCRC component

*Repository path:* `CM800A_SyncCrc_Impl/` · *AUTOSAR layer:* [Complex Device Drivers (CDD)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 10 file(s), nexteer: 16 file(s), renesas: 1 file(s), vector: 9 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `CDD_SyncCrc.c`, `CDD_SyncCrcNonRte.c` |
| `include/` (2 header(s)) | `CDD_SyncCrc.h`, `CDD_SyncCrc_private.h` |
| `autosar/` (4 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml`, `SyncCrc_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `SyncCrcInit0`
- `Calc16BitCrc_u16_Oper`
- `Calc16BitCrc_u08_Oper`
- `Calc32BitCrc_u16_Oper`
- `Calc32BitCrc_u32_Oper`
- `Calc32BitCrc_u08_Oper`
- `Calc8BitCrc0X2F_Oper`
- `Calc8BitCrc_Oper`
- `ResvCrcHwUnit_Oper`
- `Crc_CalculateCRC8`
- `Crc_CalculateCRC8H2F`
- `Crc_CalculateCRC16`
- `Crc_CalculateCRC32`
- `RelsCrcHwUnit`
- `GetAvlCrcHwUnit`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_CDD_SyncCrc.h`
- `CDD_SyncCrc_Cfg_private.h`
- `CDD_SyncCrc_private.h`
- `Os.h`
- `NxtrDet.h`
- `CDD_SyncCrc_MemMap.h`
- `CDD_SyncCrc.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [CM800A_SycnCrc_MDD](../cm800a_synccrc_impl__cm800a-sycncrc-mdd-docx/)
- [CM800A_SyncCrc_Integration_Manual](../cm800a_synccrc_impl__cm800a-synccrc-integration-manual-doc/)

Source files remain in the repository next to this documentation.

