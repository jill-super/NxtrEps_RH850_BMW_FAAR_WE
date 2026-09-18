---
title: 'CM108A_DataAndAdrPar_Impl — DataAndAdrPar Module Design Document'
description: 'Converted Word (.docx) document DataAndAdrPar Module Design Document.docx from module CM108A_DataAndAdrPar_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DataAndAdrPar Module Design Document.docx` (Word (.docx), 84 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

DataAndAdrPar

Feb 27, 2017

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

| Initial Version | Avinash James | 1 | 03/15/16 |

| Constant definition updates | Avinash James | 2 | 02/27/17 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2DataAndAdrPar & High-Level Description6

3Design details of software module7

3.1Graphical representation of DataAndAdrPar7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init:DataAndAdrParInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Init:DataAndAdrParInit29

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1ChkForECMBit289

5.4.1.1Design Rationale9

5.4.1.2Processing9

5.4.2WrTestModeCtrReg9

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale10

5.5.1.2Processing10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## DataAndAdrPar & High-Level Description

See FDD

## Design details of software module

### Graphical representation of DataAndAdrPar

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

| VCIFERRSETBFRTEST_CNT_U32 | 1 | Counts | ((uint32)1U<<0U) |

| ECMERRSETBFRTEST_CNT_U32 | 1 | Counts | ((uint32)1U<<1U) |

| READOPERECMERR_CNT_U32 | 1 | Counts | ((uint32)1U<<2U) |

| WROPERECMERR_CNT_U32 | 1 | Counts | ((uint32)1U<<3U) |

| WROPERADRPARERR_CNT_U32 | 1 | Counts | ((uint32)1U<<4U) |

| CLRERRSTSFLGFAIL_CNT_U32 | 1 | Counts | ((uint32)1U<<5U) |

| TESTMODCTRLREGWRFAIL_CNT_U32 | 1 | Counts | ((uint32)1U<<6U) |

| TOUT_CNT_U16 | 1 | Counts | 1000U |



## Software Component Implementation

### Sub-Module Functions

### Init:DataAndAdrParInit1

### Design Rationale

Non-RTE Init function to verify the Data Parity Data Transfer Path micro diagnostic. Refer FDD for more details

### Module Outputs

None

### Init:DataAndAdrParInit2

### Design Rationale

RTE empty Init function

### Module Outputs

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### ChkForEcmBit28



| Function Name | ChkForEcmBit28 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | RetVal_Cnt_T_logl | Boolean | 0 | 1 |



### Design Rationale

Static function to check whether ECM bit was set or not within a time out interval of max 2uSec

### Processing

To be called from DataAndAdrParInit1 function

### WrTestModeCtrReg



| Function Name | WrTestModCtrlReg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Val | Uint32 | 0 | 0xFFFFFFFF |

|  | ErrFlg_Cnt_T_u32 | Uint32 | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |



### Design Rationale

Static function to write to the Test Mode Control register and verify the write was successful

### Processing

To be called from DataAndAdrParInit1 function

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
