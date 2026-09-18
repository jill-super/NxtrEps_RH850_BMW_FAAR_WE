---
title: 'AR300A MotCtrlMgr'
description: 'AR300A_MotCtrlMgr_Impl (LIBS). Motor Control Manager Interrupt header'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

Motor Control Manager Interrupt header

*Repository path:* `AR300A_MotCtrlMgr_Impl/` · *AUTOSAR layer:* [Platform Libraries](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 16 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (0 C file(s)) | — |
| `include/` (2 header(s)) | `CDD_MotCtrlMgr_Irq.h`, `MotCtrlMgr_MemMap.h` |
| `autosar/` (1 ARXML) | `CDD_MotCtrlMgr_bswmd.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 1):

- `MotCtrlMgrIrq`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

No quoted `#include "..."` dependencies were found in the scanned sources.

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [MotCtrlMgr Integration Manual](../ar300a_motctrlmgr_impl__motctrlmgr-integration-manual-doc/)
- [MotCtrlMgr_MDD](../ar300a_motctrlmgr_impl__motctrlmgr-mdd-doc/)
- [MotCtrlMgr DataDictionary Tool User Guide](../ar300a_motctrlmgr_impl__motctrlmgr-datadictionary-tool-user-guide-docx/)

Source files remain in the repository next to this documentation.

