---
title: 'CF070A_BmwFltHndlg_Impl — BmwFltHndlg_MDD'
description: 'Converted Word (.docx) document BmwFltHndlg_MDD.docx from module CF070A_BmwFltHndlg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwFltHndlg_MDD.docx` (Word (.docx), 94 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

BmwFltHndlg

April 10, 2018

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

| Initial Version | Krzysztof Byrski | 1 | 6-Nov-2017 |

| Updated local constants | Krzysztof Byrski | 2 | 10-Apr-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwFltHndlg & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwFltHndlg6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwFltHndlgInit18

5.1.2Per: BmwFltHndlgPer18

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

Module Design Document for CF070A_BmwFltHndlg_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwFltHndlg & High-Level Description

BMW Fault Handling function provides a functionality of requesting the lamp status whenever the proper indicator status is set to on.

## Design details of software module

### Graphical representation of BmwFltHndlg

### Data Flow Diagram

Refer FDD

#### Component level DFD

None

#### Function level DFD

None

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

#### Init: BmwFltHndlgInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwFltHndlgPer1

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

Communication with Dem is not going through RTE.

## UNIT TEST CONSIDERATION

Create stub of Dem_GetIndicatorStatus() function.

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

| 2 | MDD Guideline EA4 | 01.00.01 |

| 3 | EA4 Software Naming Conventions | 01.01.00 |

| 4 | Software Design and Coding Standards | 2.1 |

| 5 | CF070A_BmwFltHndlg_Design | See Synergy Sub Project Version |
