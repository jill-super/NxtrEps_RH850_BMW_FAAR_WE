---
title: 'AR101A NxtrIntrpn'
description: 'AR101A_NxtrIntrpn_Impl (LIBS). Source file for the interpolation library'
---

:::tip[Origin: Custom · Nexteer in-house]
:::

## Purpose

Source file for the interpolation library

*Repository path:* `AR101A_NxtrIntrpn_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* nexteer: 3 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `NxtrIntrpn.c` |
| `include/` (2 header(s)) | `NxtrIntrpn.h`, `NxtrIntrpn_MemMap.h` |
| `autosar/` (0 ARXML) | — |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 15):

- `LnrIntrpn_u16_u16FixdXu16VariY`
- `LnrIntrpn_s16_u16FixdXs16VariY`
- `LnrIntrpn_u16_u16VariXu16VariY`
- `LnrIntrpn_u16_s16VariXu16VariY`
- `LnrIntrpn_s16_s16VariXs16VariY`
- `LnrIntrpn_s16_u16VariXs16VariY`
- `LnrIntrpnWithRound_u16_u16FixdXu16VariY`
- `LnrIntrpnWithRound_s16_u16FixdXs16VariY`
- `LnrIntrpnWithRound_u16_u16VariXu16VariY`
- `LnrIntrpnWithRound_u16_s16VariXu16VariY`
- `LnrIntrpnWithRound_s16_s16VariXs16VariY`
- `LnrIntrpnWithRound_s16_u16VariXs16VariY`
- `BilnrIntrpnWithRound_u16_u16CmnXu16MplY`
- `BilnrIntrpnWithRound_s16_u16CmnXs16MplY`
- `BilnrIntrpnWithRound_s16_s16CmnXs16MplY`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 3):

- `NxtrIntrpn.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [NxtrIntrpn Integration Manual](../ar101a_nxtrintrpn_impl__nxtrintrpn-integration-manual-doc/)

Source files remain in the repository next to this documentation.

