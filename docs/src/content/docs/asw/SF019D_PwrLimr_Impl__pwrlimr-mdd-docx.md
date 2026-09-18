---
title: 'SF019D_PwrLimr_Impl — PwrLimr_MDD'
description: 'Converted Word (.docx) document PwrLimr_MDD.docx from module SF019D_PwrLimr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PwrLimr_MDD.docx` (Word (.docx), 107 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

PwrLimr

20-APR-2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Shawn Penning,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Shawn Penning | 1.0 | 20-APR-2018 |



Table of Contents

1PwrLimr High-Level Description5

2Design details of software module6

2.1Graphical representation of PwrLimr6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: PwrLimrInit18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: PwrLimrPer18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function)………8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.1.3Per: PwrLimrPer28

4.1.3.1Design Rationale8

4.1.3.2Store Module Inputs to Local copies8

4.1.3.3(Processing of function)………8

4.1.3.4Store Local copy of outputs into Module Outputs8

4.2Server Runnables9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.4.1AssiLimCdn9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## PwrLimr High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of PwrLimr

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| BIT1MASK_ULS_U08 | 1 | Uls | 2U |

| Refer DataDict.m |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: PwrLimrInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: PwrLimrPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: PwrLimrPer2

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### AssiLimCdn



| Function Name | AssiLimCdn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FildTqLim_Uls_T_f32 | float32 | 0.0F | 1.0F |

|  | BrdgVltg_Volt_T_f32 | float32 | 6.0F | 26.5F |

| Return Value | None | N/A | N/A | N/A |



#### Design Rationale

See “Asst_Lmt_Condition_Determination” block in the Simulink model of the design.

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

| 3 | EA4 Software Naming Conventions.doc | 01.01.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD – SF019D Power Limiter | See Synergy subproject version |
