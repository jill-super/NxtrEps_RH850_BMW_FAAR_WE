---
title: 'Functional safety'
description: 'ISO 26262 ASIL D safety concept pointers.'
sidebar:
  order: 2
---

## Functional safety (ISO 26262 ASIL D)

This EPS system targets **ASIL D**, the highest automotive integrity level.
Pointers into the implementation:

- **Supervision**: `WdgM` (Watchdog Manager) with supervised entities,
  `WdgIf`/`Wdg` drivers, and `Det` (Development Error Tracer) for
  development-error reporting (see [BSW](../../bsw/)).
- **MCAL protection**: `AR099A_McalErrHndlg_Impl` (MCAL error handling),
  `CM111A_VrfyCritReg_Impl` (critical-register verification),
  `CM112A_CoreVltgMonr_Impl` (core voltage monitoring),
  exception/ECM handling (`CM101A`, `CM104A`, `CM106A`, `CM107A`).
- **End-to-end protection**: `E2E` / `E2EPW` for safety-relevant
  communication, `Crc` / `CM800A_SyncCrc_Impl` for data integrity.
- **Diagnostics**: `Dem` (fault memory), `Dcm` (UDS), `ES101A_DiagcMgr_Impl`
  (central diagnostic manager with NTC debouncing and snapshot data).
- **Coding rules**: sources carry MISRA deviation annotations
  (e.g. `NXTRDEV 19.1.1` for AUTOSAR `MemMap.h` includes) and Polyspace
  analysis artefacts (`tools/Polyspace`, `DRS.txt`, BugFinder/CodeProver
  reports under module `doc/` folders).

:::caution[Safety notice]
This documentation is descriptive. Safety-relevant decisions must be based on
the versioned safety case and the authoritative Word/PDF sources, not on the
converted excerpts.
:::
