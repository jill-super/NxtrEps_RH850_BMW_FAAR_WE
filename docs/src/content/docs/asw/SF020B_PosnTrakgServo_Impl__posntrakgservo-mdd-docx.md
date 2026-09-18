---
title: 'SF020B_PosnTrakgServo_Impl — PosnTrakgServo_MDD'
description: 'Converted Word (.docx) document PosnTrakgServo_MDD.docx from module SF020B_PosnTrakgServo_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PosnTrakgServo_MDD.docx` (Word (.docx), 100 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'akhilkrishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

PosnTrakgServo

Jan 20, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Matthew Leser | 1.0 | 20-Jan-2017 |



Table of Contents

1Introduction5

1.1Purpose5

2PosnTrakgServo & High-Level Description6

3Design details of software module7

3.1Graphical representation of PosnTrakgServo7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: PosnTrakgServoInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: PosnTrakgServoPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

MDD for Position Tracking Servo.

## PosnTrakgServo & High-Level Description

Please refer FDD

## Design details of software module

### Graphical representation of PosnTrakgServo

### Data Flow Diagram

Please refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |



## Software Component Implementation

### Sub-Module Functions

### Init: PosnTrakgServoInit1

### Design Rationale

None

### Module Outputs

None

### Per: PosnTrakgServoPer1

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



| Function Name | SVReset | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PosnServoEna_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | SVResetInp_HwNwtMtr_T_f32 | Float32 |  |  |

| Return Value | SVResetOup_Uls_T_f32 | Float32 |  |  |



### Design Rationale

NA

### Processing

Please refer SVReset block of the FDD.

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

| 5 | FDD: SF020B_PosnTrakgServo_Design | See Synergy sub project version |
