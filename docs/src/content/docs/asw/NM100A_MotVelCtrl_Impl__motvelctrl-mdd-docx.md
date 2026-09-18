---
title: 'NM100A_MotVelCtrl_Impl — MotVelCtrl_MDD'
description: 'Converted Word (.docx) document MotVelCtrl_MDD.docx from module NM100A_MotVelCtrl_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotVelCtrl_MDD.docx` (Word (.docx), 106 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

MotVelCtrl

May 4, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 17-Feb-2016 |

| Input name change | Nick Saxton | 2 | 04-May-2016 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotVelCtrl High-Level Description6

3Design details of software module7

3.1Graphical representation of MotVelCtrl7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotVelCtrlInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotVelCtrlPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1GetCtrlPrm_Oper9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………9

5.2.2SetCtrlPrm_Oper9

5.2.2.1Design Rationale9

5.2.2.2(Processing of function)………9

5.2.3StopCtrl_Oper10

5.2.3.1Design Rationale10

5.2.3.2(Processing of function)………10

5.2.4StrtCtrl_Oper10

5.2.4.1Design Rationale10

5.2.4.2(Processing of function)………10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Description10

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## MotVelCtrl High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of MotVelCtrl

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| ONEOVERTWOMPLR_ULS_F32 | 1 | Cnt | 0.5 |



For other constants, refer .m file.

#### Local Constants

## Software Component Implementation

### Sub-Module Functions

### Init: MotVelCtrlInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: MotVelCtrlPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### GetCtrlPrm_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### SetCtrlPrm_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### StopCtrl_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### StrtCtrl_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | FPIDControl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotVelTarSlewed_MotRadPerSec_T_f32 | float32 | - 183500 | 183500 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | PIDCmdLimid_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |



### Description

Blocks "F_PID Control_1" , "F_PID Control_2"  and "F_PID Control_3" are of same functionality in the FDD.  This sub function corresponds to those blocks implementation.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

- None.

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

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD : NM100A_ MotVelCtrl_Design | See Synergy sub project version |
