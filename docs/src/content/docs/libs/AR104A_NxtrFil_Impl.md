---
title: 'AR104A NxtrFil'
description: 'AR104A_NxtrFil_Impl (LIBS). function prototypes and inline function definitions for the Nexteer Filter library component'
---

:::tip[Origin: Custom · Nexteer in-house]
:::

## Purpose

function prototypes and inline function definitions for the Nexteer Filter library component

*Repository path:* `AR104A_NxtrFil_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 1 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (0 C file(s)) | — |
| `include/` (1 header(s)) | `NxtrFil.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 6):

- `FilLpUpdGain`
- `FilLpUpdOutp_f32`
- `FilLpInit`
- `FilHpUpdGain`
- `FilHpUpdOutp_f32`
- `FilHpInit`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

No quoted `#include "..."` dependencies were found in the scanned sources.

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [NxtrFil Integration Manual](../ar104a_nxtrfil_impl__nxtrfil-integration-manual-doc/)

Source files remain in the repository next to this documentation.

