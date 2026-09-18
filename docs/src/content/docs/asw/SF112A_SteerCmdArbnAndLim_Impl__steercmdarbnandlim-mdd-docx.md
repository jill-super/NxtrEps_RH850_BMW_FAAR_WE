---
title: 'SF112A_SteerCmdArbnAndLim_Impl — SteerCmdArbnAndLim_MDD'
description: 'Converted Word (.docx) document SteerCmdArbnAndLim_MDD.docx from module SF112A_SteerCmdArbnAndLim_Impl.'
sidebar:
  hidden: true
---

> **Source:** `SteerCmdArbnAndLim_MDD.docx` (Word (.docx), 115 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

SteerCmdArbnAndLim

April 27, 2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Tychy, PolandChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial version | Marek Brykczyński | 1 | 27-Apr-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2SteerCmdArbnAndLim & High-Level Description5

3Design details of software module6

3.1Graphical representation of SteerCmdArbnAndLim6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: SteerCmdArbnAndLimInit18

5.1.2Per: SteerCmdArbnAndLimPer18

5.2Server Runables8

5.2.1Oper: SetManTqCmd_Oper8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1SteerCmdArbnAndLimStMac9

5.4.2SetNtcs9

5.4.3TranDeb9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

Module Design Document for SF112A_SteerCmdArbnAndLim_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## SteerCmdArbnAndLim & High-Level Description

The Steer Command Arbitration And Limit arbitrates between different sources of Motor Torque Command based on a functional safety requirements and manufacturing process. It also provides means of applying limits to Motor Torque Command related to motor operation conditions and End Of Travel situations.

## Design details of software module

### Graphical representation of SteerCmdArbnAndLim

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| - |  |  |  |



Refer FDD for local constants.

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: SteerCmdArbnAndLimInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: SteerCmdArbnAndLimPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

#### Oper: SetManTqCmd_Oper

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

#### SteerCmdArbnAndLimStMac



| Function Name | SteerCmdArbnAndLimStMac | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | LimdMotTqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | ReqdMotTqCmdEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdNotLimd_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | - | - | - | - |



#### SetNtcs



| Function Name | SetNtcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SteerCmdArbnAndLimSt_Cnt_T_u08 | const pointer to const uint8 | 0 | 4 |

| Return Value | - | - | - | - |



#### TranDeb



| Function Name | TranDeb | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdNotLimd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | TranCond_Cnt_T_u08 | uint8 | 2 | 3 |

|  | TiThd_MilliSec_T_u16 | uint16 | FALSE | TRUE |

|  | DebTiStor_Cnt_T_u32 | const pointer to uint32 | 0 | 4294967295 |

| Return Value | DebRes_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

## Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document. (See references) |



## Glossary

Note: Terms and definitions from the source “Nexteer Automotive” take precedence over all other definitions of the same term.  Terms and definitions from the source “Nexteer Automotive” are formulated from multiple sources, including the following:

- ISO 9000

- ISO/IEC 12207

- ISO/IEC 15504

- Automotive SPICE® Process Reference Model (PRM)

- Automotive SPICE® Process Assessment Model (PAM)

- ISO/IEC 15288

- ISO 26262

- IEEE Standards

- SWEBOK

- PMBOK

- Existing Nexteer Automotive documentation



| Term | Definition | Source |

| --- | --- | --- |

| MDD | Module Design Document |  |

| DFD | Data Flow Diagram |  |



## References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.4.0 R4.0 Rev 3 |

| 2 | MDD Guideline EA4 | 1.02 |

| 3 | EA4 Software Naming Conventions | 1.01 |

| 4 | Software Design and Coding Standards | 2.01 |

| 5 | SF112A_SteerCmdArbnAndLim_Design | See Synergy Sub Project Version |
