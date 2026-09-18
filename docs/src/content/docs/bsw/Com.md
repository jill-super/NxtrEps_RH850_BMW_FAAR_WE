---
title: 'Com Com'
description: 'Com (BSW). MICROSAR Communication header file * * \details This is the implementation of the MICROSAR Communication module. * The b'
---

:::tip[Origin: Vector-provided · MICROSAR]
Project-configured/generated for this ECU (DaVinci/MICROSAR tooling).
:::

## Purpose

MICROSAR Communication header file * * \details This is the implementation of the MICROSAR Communication module. * The basic software module is based on the AUTOSAR Communication specification.

*Repository path:* `Com/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 2 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `Com.c` |
| `include/` (1 header(s)) | `Com.h` |
| `autosar/` (3 ARXML) | `Com_SafeBSW_pre.arxml`, `Com_bswmd.arxml`, `Com_preo.arxml` |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Com_Init`
- `Com_InitMemory`
- `Com_DeInit`
- `Com_IpduGroupControl`
- `Com_ReceptionDMControl`
- `Com_IpduGroupStart`
- `Com_IpduGroupStop`
- `Com_EnableReceptionDM`
- `Com_DisableReceptionDM`
- `Com_GetConfigurationId`
- `Com_GetStatus`
- `Com_GetVersionInfo`
- `Com_TriggerIPDUSend`
- `Com_TriggerIPDUSendWithMetaData`
- `Com_ClearIpduGroupVector`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 4):

- `Com.h`
- `Com_Lcfg.h`
- `SchM_Com.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_Com](../com__technicalreference-com-pdf/)

Source files remain in the repository next to this documentation.

