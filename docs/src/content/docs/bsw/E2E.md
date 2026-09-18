---
title: 'E2E E2E'
description: 'E2E (BSW). E2E header file * * \details E2E protection ensures data exchange which is protected at runtime against the effects of f'
---

:::tip[Origin: Vector-provided · MICROSAR]
:::

## Purpose

E2E header file * * \details E2E protection ensures data exchange which is protected at runtime against the effects of faults within * the communication link. E2E Library provides mechanisms for E2E protection, adequate for safety-related *

*Repository path:* `E2E/` · *AUTOSAR layer:* [Basic Software (BSW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (4 C file(s)) | `E2E.c`, `E2E_P01.c`, `E2E_P05.c`, `E2E_SM.c` |
| `include/` (4 header(s)) | `E2E.h`, `E2E_P01.h`, `E2E_P05.h`, `E2E_SM.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `make/*.mak`, `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `E2E_GetVersionInfo`
- `E2E_P01Protect`
- `E2E_P01ProtectInit`
- `E2E_P01Check`
- `E2E_P01CheckInit`
- `E2E_P01MapStatusToSM`
- `E2E_P05Protect`
- `E2E_P05ProtectInit`
- `E2E_P05Check`
- `E2E_P05CheckInit`
- `E2E_P05MapStatusToSM`
- `E2E_SMCheck`
- `E2E_SMCheckInit`
- `E2E_P01ProtectVerifyInputs`
- `E2E_P01CheckVerifyInputs`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 5):

- `E2E.h`
- `E2E_P01.h`
- `MemMap.h`
- `E2E_P05.h`
- `E2E_SM.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [TechnicalReference_E2E](../e2e__technicalreference-e2e-pdf/)

Source files remain in the repository next to this documentation.

