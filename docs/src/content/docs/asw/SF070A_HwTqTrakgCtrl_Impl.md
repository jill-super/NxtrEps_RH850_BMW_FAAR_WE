---
title: 'SF070A HwTqTrakgCtrl'
description: 'SF070A_HwTqTrakgCtrl_Impl (ASW). This component is used to calculate motor torque command from estimated torsion bar states, handwheel torque command and'
---

:::tip[Origin: Custom · Nexteer in-house]
File scaffolding in this module was generated with the Vector MICROSAR RTE Generator (DaVinci tooling); the application logic itself is in-house.
:::

## Purpose

This component is used to calculate motor torque command from estimated torsion bar states, handwheel torque command and tracking control gains.

*Repository path:* `SF070A_HwTqTrakgCtrl_Impl/` · *AUTOSAR layer:* [Application Software (ASW)](../) · *Implementation tag:* `Impl (implementation package)`

*Classification evidence (header scan of `*.c`/`*.h`):* gen: 8 file(s), nexteer: 13 file(s), vector: 8 file(s).

## Key files

| Area | Files |
| --- | --- |
| `src/` (1 C file(s)) | `HwTqTrakgCtrl.c` |
| `include/` (1 header(s)) | `HwTqTrakgCtrl.h` |
| `autosar/` (3 ARXML) | `DataTypes.arxml`, `Packages.arxml`, `PortInterfaces.arxml` |
| Build/config | `tools/` |
| Review artefacts | 1 spreadsheet checklist(s) (`*.xls*`, not converted) |

## Public API (excerpt)

Detected `FUNC(...)` entry points in headers/sources (first 3):

- `HwTqTrakgCtrlInit1`
- `HwTqTrakgCtrlPer1`
- `HwTqTrakgCtrl_Init`

Typical lifecycle: `…_Init` → runnables / cyclic processing → `…_GetVersionInfo` / `…_DeInit` where applicable.

## Dependencies (excerpt)

Direct quoted includes found in `src/*.c` (first 2):

- `HwTqTrakgCtrl.h`
- `HwTqTrakgCtrl_MemMap.h`

## Documents

Converted from the module `doc/` folder (Word/PDF → Markdown excerpts):

- [HwTqTrakgCtrl_IntegrationManual](../sf070a_hwtqtrakgctrl_impl__hwtqtrakgctrl-integrationmanual-doc/)
- [HwTqTrakgCtrl_MDD](../sf070a_hwtqtrakgctrl_impl__hwtqtrakgctrl-mdd-docx/)

Source files remain in the repository next to this documentation.

