---
title: 'CF081A_BmwTunSetHndlr_Impl — BmwTunSetHndlr_MDD'
description: 'Converted Word (.docx) document BmwTunSetHndlr_MDD.docx from module CF081A_BmwTunSetHndlr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwTunSetHndlr_MDD.docx` (Word (.docx), 148 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

BmwTunSetHndlr

May 17, 2018

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

| Initial version | Krzysztof Byrski | 1 | 27-Mar-2018 |

| Updates per design 2.0.0 | Marek Brykczyński | 2 | 10-Apr-2018 |

| Updates per design 3.0.0 | Krzysztof Byrski | 3 | 17-May-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwTunSetHndlr & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwTunSetHndlr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwTunSetHndlrInit18

5.1.2Per: BmwTunSetHndlrPer18

5.2Server Runables9

5.2.1TunVrntRead_Oper9

5.2.2TunVrntWr_Oper9

5.2.3MotVrntRead_Oper9

5.2.4MotVrntWr_Oper9

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

Module Design Document for CF081A_BmwTunSetHndlr_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwTunSetHndlr & High-Level Description

The BMW Tuning Set Handler provides a desired Runtime Index of an integer type. As the input, the function receives the desired Runtime Index. If a received value is valid then the function maps it to one of three defined values. If the proper calibration is set then the function allows overriding the output to a calibratable value. The function provides two server runnables in order to write to and to read from the NVM. During the initialization, it evaluates if the NVM is valid, if the NVM is detected invalid then it stores a predefined constant.

## Design details of software module

### Graphical representation of BmwTunSetHndlr

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

#### Init: BmwTunSetHndlrInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwTunSetHndlrPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

#### TunVrntRead_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### TunVrntWr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### MotVrntRead_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### MotVrntWr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

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

| 5 | CF081A_BmwTunSetHndlr_Design | See Synergy Sub Project Version |
