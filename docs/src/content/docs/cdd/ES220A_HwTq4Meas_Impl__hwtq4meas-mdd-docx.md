---
title: 'ES220A_HwTq4Meas_Impl — HwTq4Meas_MDD'
description: 'Converted Word (.docx) document HwTq4Meas_MDD.docx from module ES220A_HwTq4Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `HwTq4Meas_MDD.docx` (Word (.docx), 134 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

HwTq4Meas

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

| Updated to design revision 1.7.0 | Avinash James | 2.0 | 30-Nov-2016 |

| Updated as per FDD revision 1.10.0 | TATA | 3.0 | 30-Oct-2017 |



Table of Contents

1Introduction6

1.1Purpose6

2HwTq4Meas & High-Level Description7

3Design details of software module8

3.1Graphical representation of HwTq4Meas8

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1.1Init: HwTq4Meas_Init110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: HwTq4Meas_Per110

5.1.2.1Design Rationale10

5.1.3Per: HwTq4Meas_Per210

5.1.3.1Design Rationale10

5.1.4Per: HwTq4Meas_Per310

5.1.4.1Design Rationale10

5.1.5Per: HwTq4Meas_Per410

5.1.5.1Design Rationale10

5.2Server Runables10

5.2.1HwTq4AutTrim_Oper10

5.2.1.1Design Rationale10

5.2.2HwTq4ClrSnsrSca_Oper10

5.2.2.1Design Rationale10

5.2.3HwTq4ClrTrim_Oper11

5.2.3.1Design Rationale11

5.2.4HwTq4ReadSnsrSca_Oper11

5.2.4.1Design Rationale11

5.2.5HwTq4ReadTrim_Oper11

5.2.5.1Design Rationale11

5.2.6HwTq4TrimPrfmdSts_Oper11

5.2.6.1Design Rationale11

5.2.7HwTq4WrSnsrSca_Oper11

5.2.7.1Design Rationale11

5.2.8HwTq4WrTrim_Oper11

5.2.8.1Design Rationale11

5.2.9HwTq4SnsrScaPrfmdSts_Oper11

5.2.9.1Design Rationale11

5.3Module Internal (Local) Functions11

5.3.1Local Function #111

5.3.1.1Design Rationale12

5.3.1.2Processing12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

MDD for HwTq4Meas.

## HwTq4Meas & High-Level Description

## Design details of software module

Please refer to the FDD.

### Graphical representation of HwTq4Meas

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

### Init: HwTq4Meas_Init1

### Design Rationale

None

### Module Outputs

None

### Per: HwTq4Meas_Per1

### Design Rationale

Rte_Pim_HwTq4RawFastAdcIdxCntr is used in this periodic as a counter that increments from 0 to 7 and is used to write to an output buffer MotCtrlHwTq4RawFastAdcBuf accessed by Motor Control Manager. Whereas the FDD describes this counter as 1 based indexing that increments from 1 till 8.  Effective they are same in terms of functionality.

### Per: HwTq4Meas_Per2

### Design Rationale

None

### Per: HwTq4Meas_Per3

### Design Rationale

None

### Per: HwTq4Meas_Per4

### Design Rationale

None

### Server Runables

### HwTq4AutTrim_Oper

### Design Rationale

None

### HwTq4ClrSnsrSca_Oper

### Design Rationale

None

### HwTq4ClrTrim_Oper

### Design Rationale

None

### HwTq4ReadSnsrSca_Oper

### Design Rationale

None

### HwTq4ReadTrim_Oper

### Design Rationale

None

### HwTq4TrimPrfmdSts_Oper

### Design Rationale

None

### HwTq4WrSnsrSca_Oper

### Design Rationale

None

### HwTq4WrTrim_Oper

### Design Rationale

None

### HwTq4SnsrScaPrfmdSts_Oper

### Design Rationale

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | HwTqQlfr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NtcSts_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES (0U) | SIGQLFR_FAILD (2U) |

|  | ParamByte_Cnt_T_u08 | uint8 | 0 | 4 |

|  | * HwTq4Qlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES (0U) | SIGQLFR_FAILD (2U) |

| Return Value | NA | NA | NA | NA |



### Design Rationale

### Processing

Please refer to the below path in the FDD model.

ES220A_HwTq4Meas/HwTq4Meas/HwTq4MeasPer2/HwTqQlfr

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

Rte_Pim_HwTq4PrevRollgCntr is being used as a rolling counter. Hence the overflow is intentional.

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

| 5 | ES220A_HwTq4Meas_Design | See Synergy subproject version |
