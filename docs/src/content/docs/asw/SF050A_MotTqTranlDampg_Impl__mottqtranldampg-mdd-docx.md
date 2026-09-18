---
title: 'SF050A_MotTqTranlDampg_Impl — MotTqTranlDampg_MDD'
description: 'Converted Word (.docx) document MotTqTranlDampg_MDD.docx from module SF050A_MotTqTranlDampg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotTqTranlDampg_MDD.docx` (Word (.docx), 111 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

Transistional Damping (SF-50A)

August 12, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Kanth Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | EA4 01.00.01 | 12-Aug-2015 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotTqTranlDampg & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotTqTranlDampg7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: MotTqTranlDampgInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: MotTqTranlDampgPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.4.2Local Function #211

5.4.2.1Design Rationale11

5.4.2.2Processing11

5.5GLOBAL Function/Macro Definitions11

5.5.1GLOBAL Function #111

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

MDD for Motor Torque Transistional Damping.

### Scope

## MotTqTranlDampg & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of MotTqTranlDampg

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

#### Init: MotTqTranlDampgInit1

### Design Rationale

None

### Module Outputs

None

### Per: MotTqTranlDampgPer1

### Design Rationale

None

### Store Module Inputs to Local copies

Please refer FDD

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | SwOpCtrlPart1 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TranlDampgTiElpsd_MilliSec_T_f32 | float32 | 0.0 | 1000.0 |

|  | AbslMotVelCrf_MotRadPerSec_T_f32 | float32 | 0.0 | 1350.0 |

| Return Value | MotTqTranlDampgCmpl_Cnt_T_lgc | boolean | FALSE | TRUE |



### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “SwOutputCntrl” block of the Simulink model of the design.

### Local Function #2



| Function Name | SwOpCtrlPart2 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsCtrldShtDwnFltPrsnt_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | CtrlDampTrq_MotNwtMtr_T_f32 | float32 | -3.0 | 3.0 |

|  | SysSt_Cnt_T_enum | SysSt1 | 0 | 3 |

|  | MotTqCmdCrf_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | MotTqTranlDampgCmpl_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | MotTqCmdCrfDampd_MotNwtMtr_T_f32 | float32 | -11.8 | 11.8 |



### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “SwOutputCntrl” block of the Simulink model of the design.

### GLOBAL Function/Macro Definitions

None

### GLOBAL Function #1



| Function Name | NA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | NA |  |  |  |



## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |



#### Glossary

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



#### References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

| 5 | FDD : SF050A_MotTqTranlDampg_Design (V 1.1.0) | See Synergy sub project version |
