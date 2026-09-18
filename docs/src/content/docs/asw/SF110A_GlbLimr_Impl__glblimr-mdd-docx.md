---
title: 'SF110A_GlbLimr_Impl — GlbLimr_MDD'
description: 'Converted Word (.docx) document GlbLimr_MDD.docx from module SF110A_GlbLimr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `GlbLimr_MDD.docx` (Word (.docx), 101 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

GlbLimr

April 20, 2018

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

| Initial version | Marek Brykczyński | 1 | 20-Apr-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2GlbLimr & High-Level Description5

3Design details of software module6

3.1Graphical representation of GlbLimr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: GlbLimr_Init18

5.1.2Per: GlbLimr_Per18

5.2Server Runnables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1GlbLimrCompensator9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

MDD for SF110A_GlbLimr_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## GlbLimr & High-Level Description

The Global Limiter software component defines safe operating conditions and applies limits to a motor torque command based on these conditions.

## Design details of software module

<The Data Flow Diagrams should be created in the absence of this representation with the FDD.>

### Graphical representation of GlbLimr

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

| D_NUMLOOPS_CNT | 1 | Cnt | 2 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: GlbLimr_Init1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: GlbLimr_Per1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### GlbLimrCompensator



| Function Name | GlbLimrCompensator | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Assist_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | GlbLimrNotchNumberFil1_Uls_T_f32 | float32 | -1000000000 | 1000000000 |

|  | GlbLimrNotchNumberFil2_Uls_T_f32 | float32 | -1000000000 | 1000000000 |

| Return Value | CompAssist_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |



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

| 5 |  | See Synergy Sub Project Version |
