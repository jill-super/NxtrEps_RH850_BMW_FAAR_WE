---
title: 'AR100A NxtrMath'
description: 'AR100A_NxtrMath_Impl (LIBS). Nexteer Math Library Header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Nexteer Math Library Header

*Repository path:* `AR100A_NxtrMath_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 14 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (2 C file(s)) | `NxtrMath.c`, `NxtrMathNonRte.c` |
| `include/` (2 header(s)) | `NxtrMath.h`, `NxtrMath_private.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 2 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `Blnd_f32`
- `Abslt_u08_s08`
- `Abslt_u16_s16`
- `Abslt_u32_s32`
- `Abslt_f32_f32`
- `Sign_s08_s08`
- `Sign_s08_s16`
- `Sign_s08_s32`
- `Sign_s08_f32`
- `Min_s08`
- `Min_u08`
- `Min_s16`
- `Min_u16`
- `Min_s32`
- `Min_u32`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 7):

- `Rte_NxtrMath.h`
- `NxtrMath_private.h`
- `NxtrMath_MemMap.h`
- `Std_Types.h`
- `NxtrMath.h`
- `McuErrInj.h`
- `MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [NxtrMath Integration Manual](../ar100a_nxtrmath_impl__nxtrmath-integration-manual-doc/)
- [Optimized SinCos Algorithm Rev 001](../ar100a_nxtrmath_impl__optimized-sincos-algorithm-rev-001-docx/)

Source files remain in the repository next to this documentation.

