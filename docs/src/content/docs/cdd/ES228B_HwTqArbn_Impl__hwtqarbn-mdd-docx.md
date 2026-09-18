---
title: 'ES228B_HwTqArbn_Impl — HwTqArbn_MDD'
description: 'Converted Word (.docx) document HwTqArbn_MDD.docx from module ES228B_HwTqArbn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `HwTqArbn_MDD.docx` (Word (.docx), 98 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

HwTqArbn

26-May-2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

SEPG,

Nexteer Automotive,

Saginaw, MI, USAChange History



| SI. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Basavaraja Ganeshappa | 1.0 | 26th May 2016 |



Table of Contents

1HwTrqArbn High-Level Description4

2Design details of software module5

2.1Graphical representation of HwTrqArbn5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: HwTrqArbnInit17

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.1.2Per: HwTrqArbnPer17

4.1.2.1Design Rationale7

4.1.2.2Store Module Inputs to Local copies7

4.1.2.3(Processing of function)………7

4.1.2.4Store Local copy of outputs into Module Outputs7

4.2Server Runables7

4.3Interrupt Functions7

4.4Module Internal (Local) Functions7

4.4.1Local Function #17

4.4.1.1Design Rationale8

4.4.1.2Processing8

4.5GLOBAL Function/Macro Definitions8

5Known Limitations with Design9

6UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## HwTrqArbn High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of HwTrqArbn

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

Refer DD

## Software Component Implementation

Refer FDD

### Sub-Module Functions

Refer FDD

#### Init: HwTrqArbnInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: HwTrqArbnPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | FricLearning | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollgCntr_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | enum | 0 | 2 |

|  | kMaxStallCnt_Cnt_T_u08 | Uint8 | 10 |  |

|  | LstRollgCntr_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | StallCntr_Cnt_T_u08 | Uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_logl | boolean | FALSE | TRUE |



### Design Rationale

### Processing

Refer FDD

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |



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

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | Process 04.02.01 |

| 2 | MDD Guideline | Process 04.02.01 |

| 3 | Software Naming Conventions.doc | Process 04.02.01 |

| 4 | Software Design and Coding Standards.doc | Process 04.02.01 |

| 5 | ES228B_HwTqArbn_Design | Refer synergy subproject version |
