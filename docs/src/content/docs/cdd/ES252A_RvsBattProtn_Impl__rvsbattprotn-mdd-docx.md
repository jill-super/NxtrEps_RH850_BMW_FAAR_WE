---
title: 'ES252A_RvsBattProtn_Impl — RvsBattProtn_MDD'
description: 'Converted Word (.docx) document RvsBattProtn_MDD.docx from module ES252A_RvsBattProtn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `RvsBattProtn_MDD.docx` (Word (.docx), 104 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

RvsBattProtn

October 16, 2017

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

| Initial Version | Krzysztof Byrski | 1 | 16-Oct-2017 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2RvsBattProtn & High-Level Description5

3Design details of software module6

3.1Graphical representation of RvsBattProtn6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: RvsBattProtn_Init<n>8

5.1.2Per: RvsBattProtn_Per<n>8

5.2Server Runables8

5.2.1<Server Runable Name>8

5.3Interrupt Functions9

5.3.1Interrupt Function Name9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.5GLOBAL Function/Macro Definitions9

5.5.1GLOBAL Function #19

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

Module Design Document for ES252A_RvsBattProtn_Impl

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## RvsBattProtn & High-Level Description

Refer FDD.

## Design details of software module

This module provides diagnostics of Reverse Battery Protection Module. Main task is to detect opened Reverse Protection MOSFET channel.

### Graphical representation of RvsBattProtn

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

| RVSBATTPROTN_FLTTYPADCFAILD_CNT_U08 | 1 | Cnt | 4 |

| RVSBATTPROTN_FLTTYPOOR_CNT_U08 | 1 | Cnt | 2 |

| RVSBATTPROTN_FLTTYPRVSFLT_CNT_U08 | 1 | Cnt | 1 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: RvsBattProtnInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: RvsBattProtnPer1

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

This component uses config params for some configurable constants. However for testing these in PIL/SIL, please use the following strategy:

- Rename the RvsBattProtn_Cfg_PIL.h file in tools/local/include folder to RvsBattProtn_Cfg.h

- Replace the RvsBattProtn_Cfg.h file in tools/local/generate folder with the above file.

Now, Tessy must be able to modify the values of these config params. We should then test them with the range that is given in their definition in the DataDict.m file.

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

| 5 | ES252A_RvsBattProtn_Design | See Synergy Sub Project Version |
