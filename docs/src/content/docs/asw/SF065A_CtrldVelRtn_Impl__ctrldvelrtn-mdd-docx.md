---
title: 'SF065A_CtrldVelRtn_Impl — CtrldVelRtn_MDD'
description: 'Converted Word (.docx) document CtrldVelRtn_MDD.docx from module SF065A_CtrldVelRtn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CtrldVelRtn_MDD.docx` (Word (.docx), 96 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Vignesh L S K', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

CtrldVelRtn

OCT 17,2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA

TRIVANDRUM, INDIA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | TATA | 1.0 | 17-Oct-2017 |



Table of Contents

1Introduction5

1.1Purpose5

2CtrldVelRtn & High-Level Description6

3Design details of software module7

3.1Graphical representation of CtrldVelRtn7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1 Init: CtrldVelRtnInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: CtrldVelRtnPer110

5.1.1.3Design Rationale10

5.1.1.4Store Module Inputs to Local copies10

5.1.1.5(Processing of function)………10

5.1.1.6Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.4.2Local Function #211

5.4.2.1Design Rationale11

5.4.2.2Processing11

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

MDD for Controlled Velocity Return.

## CtrldVelRtn & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of CtrldVelRtn

### Data Flow Diagram

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer Data Dictionary .m file | NA | NA | NA |

| IDX2_CNT_U08 | Uint8 | CNT | 2U |

| IDX3_CNT_U08 | Uint8 | CNT | 3U |

| IDX4_CNT_U08 | Uint8 | CNT | 4U |

| IDX5_CNT_U08 | Uint8 | CNT | 5U |



## Software Component Implementation

### Sub-Module Functions

#### 5.1.1 Init: CtrldVelRtnInit1

### Design Rationale

None

### Module Outputs

None

#### 5.1.2Per: CtrldVelRtnPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

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



| Function Name | DrvrTqSeln | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdPwrLimd_MotNwtMtr_T_f32 | float32 | -8.8F | 8.8F |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10.0F | 10.0F |

|  | HwAgCmp_HwDeg_T_f32 | float32 | -1440.0F | 1440.0F |

|  | HwVel_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |

|  | AssiMechPolarity_Uls_T_s08 | sint8 | -1U | 1U |

| Return Value | DrvrTq_HwNwtMtr_T_f32 | float32 | -10.0F | 10.0F |



### Design Rationale

None.

### Processing

Refer to the “DriverTorque Selector” block of the Simulink model of the design.

### Local Function #2



| Function Name | Dampg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwVel_HwDegPerSec_T_f32 | float32 | -2406.0F | 2406.0F |

|  | CtrlSca_Uls_T_f32 | float32 | 0.0F | 1.0F |

|  | VehSpd_Kph_T_u9p7 | Uint16 | 0U | 65535U |

| Return Value | DampgTerm_HwNwtMtr_T_f32 | float32 | -100.0F | 100.0F |



### Design Rationale

None.

### Processing

Refer to the “Damping” block of the Simulink model of the design.

### GLOBAL Function/Macro Definitions

None.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

None.

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

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD : SF065A_CtrldVelRtn_Design | See Synergy Sub-project version |
