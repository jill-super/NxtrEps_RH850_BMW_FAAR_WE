---
title: 'Vector vs in-house code'
description: 'How module origin is classified in this documentation.'
sidebar:
  order: 4
---

## Vector vs in-house code

Every module page carries an **origin badge**. Four origins are distinguished:

| Origin | Meaning | How to recognise it |
| --- | --- | --- |
| **Vector-provided · MICROSAR** | Third-party BSW from Vector Informatik (COM stack, memory stack, diagnostics, OS, RTE, FlexRay, E2E, CRC, WdgM, IoHwAb). | `Copyright … Vector Informatik GmbH`, `MICROSAR` file headers, `TechnicalReference_*.pdf` docs. |
| **BMW-provided · BAC** | Third-party platform modules from the BMW AUTOSAR Core (`Rmh`, `BUtil`, `Dlog`, `Coding`, `Darh`, `Omc`, `StdDiag`, `SysTime`, `Stm`, `Srv`, `Crypto`, `Vin`). | `BMW AG` copyright, `BMW AUTOSAR Core` / `BAC` project tags. |
| **Renesas-provided · MCAL** | Microcontroller drivers for the RH850/P1x (`Mcu`, `Port`, `Dio`, `Spi`, `Fls`, `Wdg`). | `Renesas Electronics Corporation` copyright. |
| **Custom · Nexteer in-house** | Application and driver code developed for this EPS program (`SF*`, `CF*`, `ES*`, `CM*`, `MM*`, `AR*`, `NM*`, `DF*`, tools, integration). | `Nexteer` copyright and version-log headers. Many carry Vector-**generated** RTE scaffolding (`MICROSAR RTE Generator` banner) — the generator output is a template; the control logic is in-house. |

Module counts in this snapshot:

- Vector-provided: **28** · BMW-provided: **14** · Renesas-provided: **7** · Custom: **162**

> **Licensing note:** the repository root carries an MIT `LICENSE` for the
> documentation and glue added by this project. Third-party files keep their
> own proprietary headers (Vector / BMW / Renesas / Nexteer); those headers
> remain authoritative for the respective files.
