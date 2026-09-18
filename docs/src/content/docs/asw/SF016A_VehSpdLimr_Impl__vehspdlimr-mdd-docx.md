---
title: 'SF016A_VehSpdLimr_Impl — VehSpdLimr_MDD'
description: 'Converted Word (.docx) document VehSpdLimr_MDD.docx from module SF016A_VehSpdLimr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `VehSpdLimr_MDD.docx` (Word (.docx), 98 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Sarika Natu', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 4

## Converted content

For

VehSpdLimr

August 10, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sarika Natu ,

KPIT Technologies,

IndiaChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sarika Natu(KPIT Technologies) | 1.0 | 10-Aug-2015 |



Table of Contents

1VehSpdLimr High-Level Description4

2Design details of software module5

2.1Graphical representation of VehSpdLimr5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: VehSpdLimr_Init7

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.1.2Per: VehSpdLimr_Per17

4.1.2.1Design Rationale7

4.1.2.2Store Module Inputs to Local copies7

4.1.2.3(Processing of function)………7

4.1.2.4Store Local copy of outputs into Module Outputs7

4.2Server Runables7

4.3Interrupt Functions7

4.4Module Internal (Local) Functions7

4.5GLOBAL Function/Macro Definitions7

5Known Limitations with Design8

6UNIT TEST CONSIDERATION9

Appendix AAbbreviations and Acronyms10

Appendix BGlossary11

Appendix CReferences12

## VehSpdLimr High-Level Description

The Vehicle Speed Limiting Function determines a limited assist torque command value as a function of vehicle speed and handwheel position to manage mechanical fatigue near end-of-travel positions.

## Design details of software module

### Graphical representation of VehSpdLimr

### Data Flow Diagram

See FDD.

#### Component level DFD

See FDD.

#### Function level DFD

See FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

NA

## Software Component Implementation

### Sub-Module Functions

### Init<Component Name>_Init<n>

### Design Rationale

None

### Module Outputs

None

### Per: VehSpdLimrPer1

### Design Rationale

FDD model contains a block named VehSpdLimrPer1

### Store Module Inputs to Local copies

See FDD

### (Processing of function)………

See FDD

### Store Local copy of outputs into Module Outputs

See FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

Referring to anomaly EA4#1276, following are the discrepancies found:

1) Min/max values of HwAgEotCw, HwAgEotCcw, VehSpdLimrPosMaxOffs1, and VehSpdLimrPosMaxOffs2 need to be set to more realistic values; With the current ranges, there is a possiblity of converting negative numbers to unsigned data types.  Note these ranges need to be coordinated with SF011A and SF018A.

2) Table VehSpdLimrMaxAssiY monotony needs to be identified as "Decreasing" ­­ the implementation assumes that VehSpdLimrMaxAssiY[0] is the maximum value of the table.

3) The concatenate block that creates the Y table for the linear interpolation block has the two inputs reversed ­­ the first input to the concatenation should be the max value of the VehSpdLimrMaxAssiY table, and the second input to the concatenation should be the output of the 1­D Lookup block.

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

| 3 | EA4 Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | SF016A_VehSpdLimr_Design | See Synergy subproject version |
