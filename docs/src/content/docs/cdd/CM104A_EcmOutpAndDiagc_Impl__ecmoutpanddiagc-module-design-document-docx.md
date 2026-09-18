---
title: 'CM104A_EcmOutpAndDiagc_Impl — EcmOutpAndDiagc Module Design Document'
description: 'Converted Word (.docx) document EcmOutpAndDiagc Module Design Document.docx from module CM104A_EcmOutpAndDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `EcmOutpAndDiagc Module Design Document.docx` (Word (.docx), 98 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

EcmOutpAndDiagc

Feb 5, 2016

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

| Initial Version | Lucas Wendling | 1 | 10/06/15 |

| Updated with startup tests for EI and Pseudo Error Injection | Avinash James | 2 | 02/05/15 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2EcmOutpAndDiagc & High-Level Description6

3Design details of software module7

3.1Graphical representation of EcmOutpAndDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: EcmOutpAndDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Init: EcmOutpAndDiagcInit29

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.1.3Init: EcmOutpAndDiagcInit39

5.1.3.1Design Rationale9

5.1.3.2Module Outputs9

5.1.4Init: EcmOutpAndDiagcInit49

5.1.4.1Design Rationale9

5.1.4.2Module Outputs9

5.1.5Per: EcmOutpAndDiagc_Per9

5.2Server Runables10

5.2.1CtrlErrOut_Oper10

5.2.1.1Design Rationale10

5.2.1.2(Processing of function)………10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale10

5.5.1.2Processing10

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

## EcmOutpAndDiagc & High-Level Description

See FDD

## Design details of software module

### Graphical representation of EcmOutpAndDiagc

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| None |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: EcmOutpAndDiagcInit1

### Design Rationale

Temporary variables were created to read register values into in order to avoid MISRA violations that appear when volatile values are used in conditional statements.

### Module Outputs

See FDD

### Init: EcmOutpAndDiagcInit2

### Design Rationale

Empty function for purposes of memory mapping

### Module Outputs

None

### Init: EcmOutpAndDiagcInit3

### Design Rationale

Non-RTE initialization function for EI Start up Test

### Module Outputs

None

### Init: EcmOutpAndDiagcInit4

### Design Rationale

Non-RTE initialization function for Pseudo Error Injection Start up Test

### Module Outputs

None

### Per: EcmOutpAndDiagc_Per

None

### Server Runables

### CtrlErrOut_Oper

### Design Rationale

None

### (Processing of function)………

Refer to FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| EI | Exception Interrupt |



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

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |
