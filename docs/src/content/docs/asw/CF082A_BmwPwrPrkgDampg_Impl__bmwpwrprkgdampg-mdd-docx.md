---
title: 'CF082A_BmwPwrPrkgDampg_Impl — BmwPwrPrkgDampg_MDD'
description: 'Converted Word (.docx) document BmwPwrPrkgDampg_MDD.docx from module CF082A_BmwPwrPrkgDampg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwPwrPrkgDampg_MDD.docx` (Word (.docx), 161 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

BmwPwrPrkgDampg

April 18, 2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Tychy, PolandChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krzysztof Byrski | 1 | 08-Jan-2018 |

| Updates accordingly to the Design 2.0.0 (enabling/disabling functionality through a coding bit has been introduced) | Marek Brykczyński | 2 | 18-Apr-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwPwrPrkgDampg & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwPwrPrkgDampg6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwPwrPrkgDampgInit18

5.1.2Per: BmwPwrPrkgDampgPer18

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

MDD for CF082A_BmwPwrPrkgDampg_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwPwrPrkgDampg & High-Level Description

The subject function can be activated or deactivated through a coding bit. This function is responsible for determining the amount of additional motor torque damping during parking, getting to the point the power pack cannot provide the full assist anymore. The function will avoid any hard change of assist comparable to the EOT damping. The function is primarily derived from the handwheel velocity, the pinion angle and it is scaled by the vehicle velocity.

## Design details of software module

### Graphical representation of BmwPwrPrkgDampg

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

| ZERO_MOTNWTMTR_F32 | Single | MotNwtMtr | 0 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwPwrPrkgDampgInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwPwrPrkgDampgPer1

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

| 3 | EA4 Software Naming Conventions | 1.02 |

| 4 | Software Design and Coding Standards | 2.01 |

| 5 | CF082A_BmwPwrPrkgDampg_Design | See Synergy Sub Project Version |
