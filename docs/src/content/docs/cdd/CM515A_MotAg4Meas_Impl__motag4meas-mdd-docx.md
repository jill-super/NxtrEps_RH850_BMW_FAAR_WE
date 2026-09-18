---
title: 'CM515A_MotAg4Meas_Impl — MotAg4Meas_MDD'
description: 'Converted Word (.docx) document MotAg4Meas_MDD.docx from module CM515A_MotAg4Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAg4Meas_MDD.docx` (Word (.docx), 105 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Shruthi Raghavan', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

MotAg4Meas

26-Mar-2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Tata Elxsi,

Trivandrum, INDIA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Shruthi Raghavan | 1.0 | 7-Nov-16 |

| Updated unit test considerations | Tata | 2.0 | 26-Mar-2018 |



Table of Contents

1Introduction4

1.1Purpose4

2MotAg4Meas & High-Level Description5

3Design details of software module6

3.1Graphical representation of MotAg4Meas6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: MotAg4MeasInit18

5.1.2Per: None8

5.2Server Runables8

5.2.1GetMotAg4Mecl_Oper8

5.3Interrupt Functions8

5.3.1Interrupt Function Name8

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.5GLOBAL Function/Macro Definitions9

5.5.1GLOBAL Function #19

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module design document for MotAg4Meas SWC.

## MotAg4Meas & High-Level Description

Refer to design.

## Design details of software module

### Graphical representation of MotAg4Meas

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer DataDict.m file for rest of the constants.



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| REGENCA1CTLINITVAL_CNT_U16 | 1 | Cnt | 0x03U |

| REGENCA1IOC1INITVAL_CNT_U08 | 1 | Cnt | 0x04U |

| REGENCA1TTINITVAL_CNT_U08 | 1 | Cnt | 0x01U |

| REGENCA1TSINITVAL_CNT_U08 | 1 | Cnt | 0x01U |



## Software Component Implementation

### Sub-Module Functions

### Init: MotAg4MeasInit1

#### Design Rationale

Initialization of registers according to CM515A_MotAg4Meas_RegisterConfiguration.xlsm

#### Module Outputs

None

### Per: None

#### Design Rationale

#### Module Outputs

### Server Runables

#### GetMotAg4Mecl_Oper

#### Design Rationale

Refer to FDD

#### (Processing of function)………

Refer to FDD

### Interrupt Functions

None

#### Interrupt Function Name

#### Design Rationale

#### (Processing of the ISR function)…..

### Module Internal (Local) Functions

None

#### Local Function #1

#### Design Rationale

#### Processing

### GLOBAL Function/Macro Definitions

None

#### GLOBAL Function #1

#### Design Rationale

#### Processing

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

MOTAG4_SNSRRLVBITWIDTHEXP_CNT_U08 is a config param which is defined as an extern. This is defined in “CDD_MotAg4Meas_Cfg.h” tools/local/include folder. The range of this config param shall be tested.

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document |



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

| 2 | MDD Guideline | EA4 01.00 |

| 3 | Software Naming Conventions.doc | EA4 01.02 |

| 4 | Software Design and Coding Standards.doc | EA4 2.01 |

| 5 | CM515A_MotAg4Meas_Design | See Synergy subproject version |
