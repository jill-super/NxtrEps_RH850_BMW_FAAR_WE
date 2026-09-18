---
title: 'SF111A_FalbckAssi_Impl — FalbckAssi_MDD'
description: 'Converted Word (.docx) document FalbckAssi_MDD.docx from module SF111A_FalbckAssi_Impl.'
sidebar:
  hidden: true
---

> **Source:** `FalbckAssi_MDD.docx` (Word (.docx), 99 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

FalbckAssi

April 19, 2018

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

| Initial version | Krzysztof Byrski | 1 | 18-Oct-2017 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2FalbckAssi & High-Level Description5

3Design details of software module6

3.1Graphical representation of FalbckAssi6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: FalbckAssiInit18

5.1.2Per: FalbckAssiPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.5GLOBAL Function/Macro Definitions8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

Module Design Document for SF111A_FalbckAssi_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## FalbckAssi & High-Level Description

Fallback Assist shall provide assist motor torque command in a situation when system detects fault of a main motor torque generation functionality

## Design details of software module

### Graphical representation of FalbckAssi

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

| * |  |  |  |



*Refer FDD for local constants

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: FalbckAssiInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: FalbckAssiPer1

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

None

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

| 5 | SF111A_FalbckAssi_Design | See Synergy Sub Project Version |
