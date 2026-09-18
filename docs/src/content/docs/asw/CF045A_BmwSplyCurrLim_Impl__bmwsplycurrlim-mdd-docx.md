---
title: 'CF045A_BmwSplyCurrLim_Impl — BmwSplyCurrLim_MDD'
description: 'Converted Word (.docx) document BmwSplyCurrLim_MDD.docx from module CF045A_BmwSplyCurrLim_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwSplyCurrLim_MDD.docx` (Word (.docx), 143 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

BmwSplyCurrLim

May 24, 2018

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

| Initial version | Marek Brykczyński | 1 | 24-May-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwSplyCurrLim & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwSplyCurrLim6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwSplyCurrLimInit18

5.1.2Per: BmwSplyCurrLimPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1VltgDptCurrLim9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module Design Document for CF045A_BmwSplyCurrLim_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwSplyCurrLim & High-Level Description

The BMW Supply Current Limit function specifies the supply current limit based on operating conditions of the vehicle. The supply current limit is a function of vehicle speed, supply voltage measurement, customer serial communication messages and motor start stop (MSA). The function arbitrates between limits specified for each interface to meet the requirements provided by the customer.

## Design details of software module

### Graphical representation of BmwSplyCurrLim

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

| - |  |  |  |



Refer FDD for local constants.

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwSplyCurrLimInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwSplyCurrLimPer1

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

#### VltgDptCurrLim



| Function Name | VltgDptCurrLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RemCtrlPrkgEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BrdgVltg_Volt_T_u6p10 | uint16 | 6144 | 27136 |

| Return Value | A result of a conversion of fixed-point to float32 | float32 | 0 | 120 |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

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

| 5 | CF045A_BmwSplyCurrLim_Design | See Synergy Sub Project Version |
