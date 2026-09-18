---
title: 'ES209B_CurrMeasCorrln_Impl — CurrMeasCorrln_MDD'
description: 'Converted Word (.docx) document CurrMeasCorrln_MDD.docx from module ES209B_CurrMeasCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CurrMeasCorrln_MDD.docx` (Word (.docx), 106 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Sengottaiyan, Selva', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 7

## Converted content

Module Design Document

For

Current Measurement Correlation

21-Feb-2018

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

| Initial version | Nick Saxton | 1.0 | 26-Apr-2016 |

| Update per design rev. 1.6.0 | Shawn Penning | 2.0 | 23-May-2017 |

| Update graphic design 2.0 | Shawn Penning | 3.0 | 21-Feb-2018 |



Table of Contents

1Current Measurement Correlation & High-Level Description5

2Design details of software module6

2.1Graphical representation of Current Measurement Correlation6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

3.1.1.1Local7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Initialization Functions8

4.1.1.1INIT8

4.1.1.2Design Rationale8

4.1.1.3Store Module Inputs to Local copies8

4.1.1.4(Processing of function)………8

4.1.1.5Store Local copy of outputs into Module Outputs8

4.1.2PERIODIC FUNCTIONS8

4.1.2.1Per: CurrMeasCorrlnPer18

4.1.2.2Design Rationale8

4.1.2.3Store Module Inputs to Local copies8

4.1.2.4(Processing of function)………8

4.1.2.5Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions9

4.5Local Function/Macro Definitions9

4.5.1Local Function #1 SigAvlChk9

4.5.1.1Description9

4.5.2Local Function #2 CurrMeasCorrlnChk9

4.5.2.1Description9

4.6GLOBAL Function/Macro Definitions9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences15

## Current Measurement Correlation & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of Current Measurement Correlation

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

### Local



| Constant Name | Units | Value |

| --- | --- | --- |

| CORRLNSTSABC_CNT_U08 | Cnt | 0x07 |

| CURRMOTSUMLOLIM_AMPR_F32 | Ampr | 0.0F |

| CURRMOTSUMHILIM_AMPR_F32 | Ampr | 600.0F |



## Software Component Implementation

### Sub-Module Functions

### Initialization Functions

### INIT

None

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)…

None

### Store Local copy of outputs into Module Outputs

None

### PERIODIC FUNCTIONS

### Per: CurrMeasCorrlnPer1

### Design Rationale

Refer  FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)…

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function/Macro Definitions

### Local Function #1 SigAvlChk



| Function Name | SigAvlChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrQlfr1_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | MotCurrRollgCntr1_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvlABC_Cnt_T_logl | boolean | FALSE | TRUE |



### Description

Refer FDD.

### Local Function #2 CurrMeasCorrlnChk



| Function Name | CurrMeasCorrlnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrCorrdA_Ampr_T_f32 | float32 | -200 | 200 |

|  | MotCurrCorrdB_Ampr_T_f32 | float32 | -200 | 200 |

|  | MotCurrCorrdC_Ampr_T_f32 | float32 | -200 | 200 |

|  | *CurrMeasLongTermCorrlnStsVldABC_Cnt_T_logl | boolean | FALSE | TRUE |

|  | *CurrMotSumABC_Ampr_T_f32 | float32 | 0 | 600 |

| Return Value | CurrMeasImdtCorrlnStsVldABC_Cnt_T_logl | boolean | FALSE | TRUE |



### Description

Refer FDD.

* CurrMeasLongTermCorrlnStsVldABC_Cnt_T_logl  and * CurrMotSumABC_Ampr_T_f32 are  outputs of this function.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

In Signal Availability, SigQlfr sets up 3 possible results:

0 = No Result

1 = Pass

2 = Fail

The model converts this enumerated type to uint8 and checks if less than 2 (Fail). The code differs in that it checks explicitly for No Result (SIGQLFR_NORES) or Pass (SIGQLFR_PASSD).

## UNIT TEST CONSIDERATION

#### Continuous improvent CR EA4#12527 written for output range correction for CurrMeasCorrlnSts.Abbreviations and Acronyms



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

| 1 | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.01.00 |

| 3 | Software Naming Conventions | 01.01.00 |

| 4 | Software Design and Coding Standards | 2.1 |

| 5 | FDD – ES209A Current Measurement Correlation | See synergy subversion |
