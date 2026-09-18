---
title: 'CF108A_BmwSwFctDi_Impl — BmwSwFctDi_MDD'
description: 'Converted Word (.docx) document BmwSwFctDi_MDD.docx from module CF108A_BmwSwFctDi_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwSwFctDi_MDD.docx` (Word (.docx), 127 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

BmwSwFctDi

July 28, 2018

Prepared By:

Akilan Rathakrishnan,

Nexteer Automotive,

Saginaw, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial version | Akilan Rathakrishnan | 1.0 | 28-Jul-2018 |

| Updated Design rationale for periodic and init runnables | Akilan Rathakrishanan | 2.0 | 30-Jul-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2BmwSwFctDi High-Level Description6

3Design details of software module7

3.1Graphical representation of BmwVehSpd8

3.2Data Flow Diagram9

3.2.1Component level DFD9

3.2.2Function level DFD9

4Constant Data Dictionary10

4.1Program (fixed) Constants10

4.1.1Embedded Constants10

5Software Component Implementation11

5.1Sub-Module Functions11

5.1.1BmwSwFctDiInit111

5.1.1.1Design Rationale11

5.1.1.2Module Outputs11

5.1.2BmwSwFctDiPer111

5.1.2.1Design Rationale11

5.1.2.2Module Outputs11

5.2Server Runnables11

5.3Interrupt Functions11

5.3.1Interrupt Function Name11

5.4Module Internal (Local) Functions11

5.4.1UpdCodingBits11

5.4.2ReadCodingData11

5.4.3PullCmpCmdDiBmwOvrd12

5.4.4InertiaCmpVelCmdDiBmwOvrd12

5.4.5ClsdLoopHysEna12

5.4.6CtrldVelRtnEna12

5.4.7OvrdCmdEna12

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CPlease references17

## Introduction

### Purpose

Module Design Document for CF0108A_BmwSwFctDi_Impl

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwSwFctDi High-Level Description

This is BMW specific and will allow features to be disabled per customer requirements without altering multiple SF''s.  It will also take a client call from the BAC module coding and output Boolean logic to allow BMW to disable the required features.  This client call will be changing over time from BMW and this function allows change to happen in one component instead of adjusting all the CF components that need and output from this.

## Design details of software module

Please refer FDD

### Graphical representation of BmwVehSpd

### Data Flow Diagram

Please refer FDD

#### Component level DFD

Please refer FDD

#### Function level DFD

Please refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file for constants |  |  |  |



## Software Component Implementation

### Sub-Module Functions

#### BmwSwFctDiInit1

### Design Rationale

Implementation of the init runnable differs from design due to the way this component need to interact with BMW BAC Coding component.

### Module Outputs

None

### BmwSwFctDiPer1

### Design Rationale

Implementation of the periodic differs from design due to the way this component need to interact with BMW BAC Coding component.

### Module Outputs

None

### Server Runnables

None

### Interrupt Functions

None

### Interrupt Function Name

None

### Module Internal (Local) Functions

#### UpdCodingBits



| Function Name | UpdCodingBits | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CodingDataMode_Cnt_T_u08 | Uint8 | 0 | 5 |

| Return Value | None | - | - | - |



#### ReadCodingData



| Function Name | ReadCodingData | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CodingDataMode_Cnt_T_u08 | uint8 | 0 | 5 |

| Return Value | None | - | - | - |



#### PullCmpCmdDiBmwOvrd



| Function Name | VehSpdRateLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PullCmpCmdDi_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | PullCmpCmdDiBmwOvrd_Cnt_T_logl | Boolean | FALSE | TRUE |



#### InertiaCmpVelCmdDiBmwOvrd



| Function Name | InertiaCmpVelCmdDiBmwOvrd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | InertiaCmpVelCmdDi_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | InertiaCmpVelCmdDiBmwOvrd_Cnt_T_logl | boolean | FALSE | TRUE |



#### ClsdLoopHysEna



| Function Name | ClsdLoopHysEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqCmdHys_HwNwtMtr_T_f32 | Float32 | -10 | 10 |

| Return Value | HwTqCmdHysBmwOvrd_HwNwtMtr_T_f32 | Float32 | -10 | 10 |



#### CtrldVelRtnEna



| Function Name | CtrldVelRtnEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CtrldVelRtnCmd_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

| Return Value | CtrldVelRtnCmdBmwOvrd_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |



#### OvrdCmdEna



| Function Name | ProcessFourthAndGateState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | OvrdCal_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | CodingBit_Cnt_T_u08 | Uint8 | 0 | 255 |

| Return Value | OvrlCmdEna_Cnt_T_logl | boolean | FALSE | TRUE |



### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

- Client calls to BMW BAC Coding component are not listed in the design since this will require modeling 3rd party software.

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |



#### Glossary

Note: Terms and definitions from the source “Nexteer Automotive” take precedence over all other definitions of the same term.  Terms and definitions from the source “Nexteer Automotive” are formulated from multiple sources, including the following:

- ISO 9000

- ISO/IEC 12207

- ISO/IEC 15504

- Automotive SPICE® Process Please reference Model (PRM)

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



#### Please references



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD: CF108A_BmwSwFctDi_Design | See Synergy subproject version |
