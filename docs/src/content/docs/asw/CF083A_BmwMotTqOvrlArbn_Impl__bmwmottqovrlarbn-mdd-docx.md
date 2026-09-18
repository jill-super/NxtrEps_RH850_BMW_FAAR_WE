---
title: 'CF083A_BmwMotTqOvrlArbn_Impl — BmwMotTqOvrlArbn_MDD'
description: 'Converted Word (.docx) document BmwMotTqOvrlArbn_MDD.docx from module CF083A_BmwMotTqOvrlArbn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwMotTqOvrlArbn_MDD.docx` (Word (.docx), 160 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

BmwMotTqOvrlArbn

July 03, 2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial version | Krzysztof Byrski | 1 | 28-Feb-2018 |

| Updated graphical representation as per Design 2.0.0 | Krzysztof Byrski | 2 | 04-Apr-2018 |

| Updated unit test considerations | Krzysztof Byrski | 3 | 22-Jun-2018 |

| Updated graphical representation as per Design 3.0.0 | Krzysztof Byrski | 4 | 03-Jul-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwMotTqOvrlArbn & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwMotTqOvrlArbn6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwMotTqOvrlArbnInit18

5.1.2Per: BmwMotTqOvrlArbnPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1Local Function ChkForFctlErr9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module Design Document for CF083A_BmwMotTqOvrlArbn_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwMotTqOvrlArbn & High-Level Description

This function accepts multiple torque overlay commands and based on other supplied signals, it decides which of provided torque overlays should be used as torque overlay command. It also sets torque overlay command to zero if safety related conditions occur.

## Design details of software module

### Graphical representation of BmwMotTqOvrlArbn

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

| CNVMILLISECTOCNT_CNTPERMILLISEC_U16 | 1 | CntPerMilliSec | 10 |

| TWENTYCNT_CNT_U32 | 1 | Cnt | 20 |

| ZERO_MOTNWTMTR_F32 | Single Precision Float | MotNwtMtr | 0 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwMotTqOvrlArbnInit1

#### Design Rationale

Refer FDD

#### Module Outputs

None

#### Per: BmwMotTqOvrlArbnPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### Local Function ChkForFctlErr



| Function Name | ChkForFctlErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MfgModActv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwNearStillVehSpdSts_Cnt_T_enum | enum | 12 | 15 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | MfgModCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | N/A |  |  |  |



#### Design Rationale

Implementation of “ChkForFctlErr” Simulink block.

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

| 5 | CF083A_BmwMotTqOvrlArbn_Design | See Synergy Sub Project Version |
