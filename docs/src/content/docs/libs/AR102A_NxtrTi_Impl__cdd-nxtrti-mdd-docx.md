---
title: 'AR102A_NxtrTi_Impl — CDD_NxtrTi_MDD'
description: 'Converted Word (.docx) document CDD_NxtrTi_MDD.docx from module AR102A_NxtrTi_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CDD_NxtrTi_MDD.docx` (Word (.docx), 95 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Penning, Shawn', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

CDD_NxtrTi

Aug 23, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Shawn Penning,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Shawn Penning | 1.0 | 01-May-2017 |

| Updated for error injection | Avinash James | 2.0 | 23-Aug-2017 |



Table of Contents1Introduction5

1.1Purpose5

1.2Scope5

2CDD_NxtrTi & High-Level Description6

3Design details of software module7

3.1Graphical representation of CDD_NxtrTi7

3.2Data Flow Diagram7

Component level DFD7

Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: NxtrTiInit19

5.1.1.1Design Rationale9

5.1.1.2Store Module Inputs to Local copies9

5.1.1.3(Processing of function)………9

5.1.1.4Module Outputs9

5.1.2NxtrTiInit09

5.1.3Per: NxtrTiPer19

5.1.3.1Design Rationale9

5.1.3.2Store Module Inputs to Local copies9

5.1.3.3(Processing of function)………9

5.1.3.4Store Local copy of outputs into Module Outputs10

5.2Server Runnables10

5.2.1GetRefTmr100MicroSec32bit10

5.2.2GetRefTmr1MicroSec32bit10

5.2.3GetTiSpan100MicroSec32bit10

5.2.4GetTiSpan1MicroSec32bit10

5.3Interrupt Functions10

5.3.1Interrupt Function Name10

5.3.1.1Design Rationale11

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.5GLOBAL Function/Macro Definitions11

5.5.1GLOBAL Function #111

5.5.1.1Design Rationale11

5.5.1.2processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## CDD_NxtrTi & High-Level Description

Nexteer Time Complex Driver

Refer to FDD to be created under CR EA4#164

## Design details of software module

Refer to FDD to be created under CR EA4#164

### Graphical representation of CDD_NxtrTi

### Data Flow Diagram

Refer to FDD to be created under CR EA4#164

#### Component level DFD

Refer to FDD to be created under CR EA4#164

#### Function level DFD

Refer to FDD to be created under CR EA4#164

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| TMRFLTTHD_CNT_U32 | 1 | Counts | 200U |



## Software Component Implementation

Refer to FDD to be created under CR EA4#164

### Sub-Module Functions

### Init: NxtrTiInit1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer to FDD to be created under CR EA4#164

### Module Outputs

None

### NxtrTiInit0

#### Design Rationale

To be called by the user during initialization.  If timers are not required prior to starting the

*              RTE, this function does not need to be called directly by a user.

#### (Processing of function)

Non-RTE version of Nexteer Time Initialization function.  Calling this function will initialize and

*              start the hardware timers used by this module if not already done.

### Per: NxtrTiPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer to FDD to be created under CR EA4#164

### Store Local copy of outputs into Module Outputs

Refer to FDD to be created under CR EA4#164

### Server Runnables

### GetRefTmr100MicroSec32bit

#### Design Rationale

Refer to FDD to be created under CR EA4#164

#### (Processing of function)

Refer to FDD to be created under CR EA4#164

### GetRefTmr1MicroSec32bit

#### Design Rationale

Refer to FDD to be created under CR EA4#164

#### (Processing of function)

Refer to FDD to be created under CR EA4#164

### GetTiSpan100MicroSec32bit

#### Design Rationale

Refer to FDD to be created under CR EA4#164

#### (Processing of function)

Refer to FDD to be created under CR EA4#164

### GetTiSpan1MicroSec32bit

#### Design Rationale

Refer to FDD to be created under CR EA4#164

#### (Processing of function)

Refer to FDD to be created under CR EA4#164

### Interrupt Functions

None

### Interrupt Function Name

None

### Design Rationale

None

### Module Internal (Local) Functions

### Local Function #1

None



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | (if none, write None) | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

|  | (Insert more rows for additional passed arguments) |  |  |  |

| Return Value | (if no value returned, write N/A) |  |  |  |



### Design Rationale

### Processing

### GLOBAL Function/Macro Definitions

Refer to 5.1.2

### GLOBAL Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | (if none, write None) | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

|  | (Insert more rows for additional passed arguments) |  |  |  |

| Return Value | (if no value returned, write N/A) |  |  |  |



### Design Rationale

### processing

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

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |
