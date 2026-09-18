---
title: 'ES251A_BattRtnCurr_Impl — BattRtnCurr_MDD'
description: 'Converted Word (.docx) document BattRtnCurr_MDD.docx from module ES251A_BattRtnCurr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BattRtnCurr_MDD.docx` (Word (.docx), 117 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

BattRtnCurr

October 11, 2017

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

| Initial Version | Krzysztof Byrski | 1 | 21-July-2017 |

| Updated as per Design version 1.1.0 | Krzysztof Byrski | 2 | 11-October-2017 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BattRtnCurr & High-Level Description5

3Design details of software module6

3.1Graphical representation of BattRtnCurr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BattRtnCurrInit18

5.1.2Per: BattRtnCurrPer18

5.1.3Per: BattRtnCurrPer28

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module Design Document for ES251A_BattRtnCurr

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BattRtnCurr & High-Level Description

Refer FDD.

## Design details of software module

This function handles measurement of battery return current. It receives ADC samples representing current in volts and converts them to ampere units.

Additionally, it performs basic output signal limitation. Module design allows execution from motor control loop or 2ms periodic. Therefore two sets of input and outputs signals are available where ones prefixed with "MotCtrl" shall be used inside motor control loop.

### Graphical representation of BattRtnCurr

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

| BATTRTNCURRPASSD_CNT_U08 | 1 | Cnt | 0 |

| BATTRTNCURROVERMAX_CNT_U08 | 1 | Cnt | 1 |

| BATTRTNCURRUNDERMIN_CNT_U08 | 1 | Cnt | 2 |

| BATTRTNCURRFAILDADC_CNT_U08 | 1 | Cnt | 4 |

| BATTRTNCURRESTIMDIFFFLT_CNT_U08 | 1 | Cnt | 8 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BattRtnCurrInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BattRtnCurrPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

#### Per: BattRtnCurrPer2

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

| - | - |



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

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | 01.01.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | ES251A_BattRtnCurr_Design | See Synergy Sub Project Version |
