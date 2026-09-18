---
title: 'Communication'
description: 'FlexRay, COM stack and calibration interfaces.'
sidebar:
  order: 3
---

## Communication

### FlexRay (vehicle bus)

- Stack: `Fr` (driver) → `FrIf` (interface) → `FrSM` (state manager),
  `FrTp` (transport protocol), `FrTrcv_30_Tja1082` (transceiver),
  configured under `FrXcp` for measurement access (see [BSW](../../bsw/)).
- Application mapping: **18** `MM*` message-slot components
  (`MM096A…MM530A_BmwMsgSlot*`, see [ASW](../../asw/)) model individual
  FlexRay frame slots/channels for the BMW FAAR WE matrix.

### AUTOSAR COM

- `Com` (signals/groups), `ComM` (channel management), `PduR` (routing),
  `IpduM` (multiplexed PDUs).

### Diagnostics and calibration

- `Dcm`/`Dem` (UDS + fault memory), `Xcp` + `ES104B_XcpIf_Impl` (calibration),
  `E2E`/`E2EPW` (protection), `Darh`/`StdDiag`/`Dlog` (BMW BAC diagnostics).
