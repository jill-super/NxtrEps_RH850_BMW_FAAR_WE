---
title: 'ES249B_MotAgCorrln_Impl — MotAgCorrln_MDD'
description: 'Converted Word (.docx) document MotAgCorrln_MDD.docx from module ES249B_MotAgCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAgCorrln_MDD.docx` (Word (.docx), 107 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Sarika Natu', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

‘MotAgCorrln’

Jun 01, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Nick Saxton | 1.0 | 01-Jun-2016 |



Table of Contents

1Introduction5

2MotAgCorrln & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotAgCorrln7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotAgCorrlnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotAgCorrlnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3NoneInterrupt Functions9

5.3.1Interrupt Function Name9

5.3.1.1Design Rationale9

5.3.1.2(Processing of the ISR function)…..9

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #210

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale10

5.5.1.2processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

MDD for MotAgCorrln .

## MotAgCorrln & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of MotAgCorrln

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

| MOTAGMECLCORRLNSTMIN_CNT_U08 | None | Cnt | 0 |

| MOTAGMECLCORRLNSTMAX_CNT_U08 | None | Cnt | 3 |

| MOTAGMECLIDPTSIGMIN_CNT_U08 | None | Cnt | 0 |

| MOTAGMECLIDPTSIGMAX_CNT_U08 | None | Cnt | 2 |



## Software Component Implementation

### Sub-Module Functions

### Init: MotAgCorrlnInit1

Refer FDD

### Design Rationale

Design follows implementation in FDD.

### Module Outputs

Refer FDD

### Per: MotAgCorrlnPer1

Refer FDD

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer to FDD  (Block ‘MotAgCorrlnPer1’)

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### NoneInterrupt Functions

None

### Interrupt Function Name

None

### Design Rationale

None

### (Processing of the ISR function)…..

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | MtrAgSigAvlCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | Enum (SigQlfr1) | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | LstRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | LstStall_Cnt_T_u08 | uint8 | 0 | 255 |

|  | *StallCntOutp_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | FALSE | TRUE |



### Design Rationale

Checks Signal Availability of Motor. Implementation of 'MtrAgA SigAvlCheck' and 'MtrAgB SigAvlCheck' blocks.

### Processing

Note: ‘* StallCntOutp_Cnt_T_u08’ is an output of this function.

#### Local Function #2



| Function Name | TestOkCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgAMecl_MotRev_T_u0p16 | u0p16 | 0 | 65535 |

|  | MotAgBMecl_MotRev_T_u0p16 | u0p16 | 0 | 65535 |

| Return Value | TestOk_Cnt_T_logl | boolean | FALSE | TRUE |



### Design Rationale

Implementation of 'TestOk' check functionality. This function corresponds to the block 'MotAgA vs MotAgB'.

### Processing

Refer FDD.

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

None

### Design Rationale

None

### processing

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

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

| 2 | MDD Guideline | EA4 01.00.02 |

| 3 | Software Naming Conventions.doc | EA4 01.00.02 |

| 4 | Software Design and Coding Standards.doc | EA4 01.00.02 |

| 5 | ES249B_MotAgCorrln_Design | See Synergy subproject version |
