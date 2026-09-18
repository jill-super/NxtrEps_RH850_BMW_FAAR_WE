---
title: 'AR103A NxtrFixdPt'
description: 'AR103A_NxtrFixdPt_Impl (LIBS). Nexteer Fixed Point Library Header'
---

:::tip[Origin: Custom · Nexteer in-house]
:::

## Purpose

Nexteer Fixed Point Library Header

*Repository path:* `AR103A_NxtrFixdPt_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 1 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (0 C file(s)) | — |
| `include/` (1 header(s)) | `NxtrFixdPt.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 12):

- `FloatToFixdWithRound_s16_f32`
- `FloatToFixdWithRound_s32_f32`
- `FloatToFixdWithRound_u16_f32`
- `FloatToFixdWithRound_u32_f32`
- `FloatToFixd_s16_f32`
- `FloatToFixd_s32_f32`
- `FloatToFixd_u16_f32`
- `FloatToFixd_u32_f32`
- `FixdToFloat_f32_s16`
- `FixdToFloat_f32_s32`
- `FixdToFloat_f32_u16`
- `FixdToFloat_f32_u32`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

No quoted `#include "..."` dependencies were found in the scanned sources.

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [NxtrFixdPt Integration Manual](../ar103a_nxtrfixdpt_impl__nxtrfixdpt-integration-manual-doc/)

Source files remain in the repository next to this documentation.

