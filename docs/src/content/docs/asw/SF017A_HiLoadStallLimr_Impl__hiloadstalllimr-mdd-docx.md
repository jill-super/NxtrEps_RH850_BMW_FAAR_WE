---
title: 'SF017A_HiLoadStallLimr_Impl — HiLoadStallLimr_MDD'
description: 'Converted Word (.docx) document HiLoadStallLimr_MDD.docx from module SF017A_HiLoadStallLimr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `HiLoadStallLimr_MDD.docx` (Word (.docx), 111 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

HiLoadStallLimr

March 22, 2018

Prepared By:

Jayakrishnan T,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | EA4 01.00.01 | 19-Aug-2015 |

| Updated to Design Ver 2.0.0 | Matthew Leser | 2.0 | 28-Feb-2017 |

| Updated Diagram | Matthew Leser | 3.0 | 20-Oct-2017 |

| Updated Local constant values | Jayakrishnan T | 4.0 | 22-Mar-2018 |



Table of Contents

1Introduction5

1.1Purpose5

2HiLoadStallLimr & High-Level Description6

3Design details of software module7

3.1Graphical representation of HiLoadStallLimr7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: HiLoadStallLimrInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: HiLoadStallLimrPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

MDD for HiLoadStallLimr

## HiLoadStallLimr & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of HiLoadStallLimr

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

| IVTRLOABITMASK_CNT_U08 | 1 | CNT | 2U |

| FETLOABITMASK_CNT_U08 | 1 | CNT | 4U |



## Software Component Implementation

### Sub-Module Functions

None

### Init: HiLoadStallLimrInit1

### Design Rationale

### Module Outputs

None

### Per: HiLoadStallLimrPer1

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



| Function Name | None | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | NA | NA | NA |

|  | None | NA | NA | NA |

| Return Value | NA | NA | NA | NA |



### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name | NA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  | NA |  |  |  |

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

| 5 | FDD : SF017A_HiLoadStallLimr_Design | See Synergy sub project version |
