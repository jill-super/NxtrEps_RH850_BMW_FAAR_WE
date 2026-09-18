---
title: 'ES221A_HwTq5Meas_Impl — HwTq5Meas_MDD'
description: 'Converted Word (.docx) document HwTq5Meas_MDD.docx from module ES221A_HwTq5Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `HwTq5Meas_MDD.docx` (Word (.docx), 132 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

HwTq5Meas

Oct 30, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI,

TRIVANDRUM, INDIA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Anne | 1.0 | 10-Jun-2016 |

| Added a new server runnable | Avinash James | 2.0 | 01-Dec-2016 |

| Updated as per FDD revision 1.10.0 | TATA | 3.0 | 30-10-2017 |



Table of Contents

1Introduction5

1.1Purpose5

2HwTq5Meas & High-Level Description6

3Design details of software module7

3.1Graphical representation of HwTq5Meas7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1.1Init: HwTq5Meas_Init19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: HwTq5Meas_Per19

5.1.2.1Design Rationale9

5.1.3Per: HwTq5Meas_Per29

5.1.3.1Design Rationale9

5.1.4Per: HwTq5Meas_Per39

5.1.4.1Design Rationale9

5.1.5Per: HwTq5Meas_Per49

5.1.5.1Design Rationale9

5.2Server Runables9

5.2.1HwTq5AutTrim_Oper9

5.2.1.1Design Rationale9

5.2.2HwTq5ClrSnsrSca_Oper9

5.2.2.1Design Rationale9

5.2.3HwTq5ClrTrim_Oper10

5.2.3.1Design Rationale10

5.2.4HwTq5ReadSnsrSca_Oper10

5.2.4.1Design Rationale10

5.2.5HwTq5ReadTrim_Oper10

5.2.5.1Design Rationale10

5.2.6HwTq5TrimPrfmdSts_Oper10

5.2.6.1Design Rationale10

5.2.7HwTq5WrSnsrSca_Oper10

5.2.7.1Design Rationale10

5.2.8HwTq5WrTrim_Oper10

5.2.8.1Design Rationale10

5.2.9HwTq5SnsrScaPrfmdSts_Oper10

5.2.9.1Design Rationale10

5.3Module Internal (Local) Functions10

5.3.1Local Function #110

5.3.1.1Design Rationale11

5.3.1.2Processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

MDD for HwTq5Meas.

## HwTq5Meas & High-Level Description

## Design details of software module

Please refer to the FDD.

### Graphical representation of HwTq5Meas

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer to the FDD |  |  |  |



## Software Component Implementation

### Init: HwTq5Meas_Init1

### Design Rationale

None

### Module Outputs

None

### Per: HwTq5Meas_Per1

### Design Rationale

Rte_Pim_HwTq5RawFastAdcIdxCntr is used in this periodic as a counter that increments from 0 to 7 and is used to write to an output buffer MotCtrlHwTq5RawFastAdcBuf accessed by Motor Control Manager. Whereas the FDD describes this counter as 1 based indexing that increments from 1 till 8.  Effective they are same in terms of functionality.

### Per: HwTq5Meas_Per2

### Design Rationale

None

### Per: HwTq5Meas_Per3

### Design Rationale

None

### Per: HwTq5Meas_Per4

### Design Rationale

None

### Server Runables

### HwTq5AutTrim_Oper

### Design Rationale

None

### HwTq5ClrSnsrSca_Oper

### Design Rationale

None

### HwTq5ClrTrim_Oper

### Design Rationale

None

### HwTq5ReadSnsrSca_Oper

### Design Rationale

None

### HwTq5ReadTrim_Oper

### Design Rationale

None

### HwTq5TrimPrfmdSts_Oper

### Design Rationale

None

### HwTq5WrSnsrSca_Oper

### Design Rationale

None

### HwTq5WrTrim_Oper

### Design Rationale

None

### HwTq5SnsrScaPrfmdSts_Oper

### Design Rationale

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | HwTqQlfr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NtcSts_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES (0U) | SIGQLFR_FAILD (2U) |

|  | ParamByte_Cnt_T_u08 | uint8 | 0 | 4 |

|  | * HwTq5Qlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES (0U) | SIGQLFR_FAILD (2U) |

| Return Value | NA | NA | NA | NA |



### Design Rationale

### Processing

Please refer to the below path in the FDD model.

ES220A_HwTq5Meas/HwTq5Meas/HwTq5MeasPer2/HwTqQlfr

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

Rte_Pim_HwTq5PrevRollgCntr is used as a rolling counter. Hence roll over is intentional..

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

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | ES221A_HwTq5Meas_Design | See Synergy subproject version |
