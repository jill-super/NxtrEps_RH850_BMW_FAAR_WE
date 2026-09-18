---
title: 'Build system'
description: 'How the EPS firmware is configured and built.'
sidebar:
  order: 1
---

## Build system

The firmware is built per module and integrated at the top level.
There is no single root Makefile; instead each delivery unit carries its own
build description, which is characteristic for this kind of
OEM/Tier-1 mixed Vector + in-house project.

### Per-module build descriptions

- **Vector MICROSAR BSW modules** (`Com`, `PduR`, `NvM`, `Dem`, `Os`, …)
  carry `make/*.mak` quadruples (`*_defs.mak`, `*_cfg.mak`, `*_rules.mak`,
  `*_check.mak`) consumed by the overarching ECU build.
- **BMW BAC and platform modules** (`Rmh`, `BUtil`, `Coding`, `Crypto`, …)
  carry `make/CMakeListsClassic.txt` / `make/CMakeListsGeneric.txt`
  (Classic vs Generic build variants).
- **MCAL drivers** (`Mcu`, `Port`, `Dio`, `Spi`, `Fls`, `Wdg`) carry
  `make/`, `generate/` (DaVinci-generated configuration) and `tools/`.
- **Application SW-Cs / CDDs** (`SF*`, `CF*`, `ES*`, `CM*`, …) carry
  `autosar/*.arxml` (component, data types, port interfaces),
  `tools/Component.dpa` (DaVinci Developer project) and Polyspace artefacts.

### Generation flow

1. AUTOSAR authoring in **DaVinci Developer / DaVinci Configurator**
   (see [Tools](../../tools/) and the `TL102A_Davinci` module page).
2. **MICROSAR RTE and BSW generation** into `generate/` and
   `_Bmw_5441_Eps_Impl_A/generate/` (RTE contracts, `MemMap.h`,
   module configuration headers).
3. Compilation with the Green Hills toolchain
   (per-module `tools/*.gpj`, e.g. `BswM/tools/BswM.gpj`) for the
   **Renesas RH850/P1x** target, then linking and flashing.

### Flashing

Clone the repository, run generation with the licensed Vector/BMW tooling,
build the ECU image and flash it onto the Renesas RH850 controller
(details depend on the bench setup; no flashing scripts are versioned here).
