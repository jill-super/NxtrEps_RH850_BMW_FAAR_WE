---
title: 'SF111A FalbckAssi'
description: 'SF111A_FalbckAssi_Impl (ASW). SF111A Implementation - Fallback Assist'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

SF111A Implementation - Fallback Assist

*Repository path:* `SF111A_FalbckAssi_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 9 file(s), nexteer: 12 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `FalbckAssi.c` |
| `include/` (0 header(s)) | — |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 2):

- `FalbckAssiInit1`
- `FalbckAssiPer1`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 6):

- `Rte_FalbckAssi.h`
- `NxtrFixdPt.h`
- `NxtrIntrpn.h`
- `NxtrMath.h`
- `SysGlbPrm.h`
- `FalbckAssi_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [FalbckAssi_IntegrationManual](../sf111a_falbckassi_impl__falbckassi-integrationmanual-doc/)
- [FalbckAssi_MDD](../sf111a_falbckassi_impl__falbckassi-mdd-docx/)

Source files remain in the repository next to this documentation.

