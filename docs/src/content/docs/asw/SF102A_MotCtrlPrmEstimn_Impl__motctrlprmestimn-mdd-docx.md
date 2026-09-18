---
title: 'SF102A_MotCtrlPrmEstimn_Impl — MotCtrlPrmEstimn_MDD'
description: 'Converted Word (.docx) document MotCtrlPrmEstimn_MDD.docx from module SF102A_MotCtrlPrmEstimn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotCtrlPrmEstimn_MDD.docx` (Word (.docx), 98 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Binder, Brendon', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

MotCtrlPrmEstimn

06-Dec-2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Brendon Binder,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Rijvi | 1.0 | 20-JUN-2015 |

| 2 | Updated per design rev. 1.5.0 | Rijvi | 2.0 | 07-APRIL-2016 |

| 3 | Updated per design rev. 2.1.0 | ML | 3.0 | 29-NOV-2016 |

| 4 | New Input added MotAndThermProtnLoaMod and deleted IvtrLoaMtgtnEna | TATA | 4.0 | 25-SEP-2017 |

| 5 | Removed local function which didn’t exist, migrated document to latest template | BRB | 5.0 | 06-DEC-2017 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotCtrlPrmEstimn & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotCtrlPrmEstimn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotCtrlPrmEstimnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotCtrlPrmEstimnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.1.1Per: MotCtrlPrmEstimnPer29

5.1.1.1Design Rationale9

5.1.1.2Store Module Inputs to Local copies9

5.1.1.3(Processing of function)………9

5.1.1.4Store Local copy of outputs into Module Outputs9

5.2Server Runnables10

5.2.1SetMotPrmNomEol10

5.2.1.1Design Rationale10

5.2.1.2(Processing of function)………10

5.2.2SetMotPrmNomEol10

5.2.2.1Design Rationale10

5.2.2.2(Processing of function)………10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## MotCtrlPrmEstimn & High-Level Description

Please refer FDD

## Design details of software module

### Graphical representation of MotCtrlPrmEstimn

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

| BITMASK2_CNT_U08 | 1 | Cnt | 2U |

| Refer constants from .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

#### Init: MotCtrlPrmEstimnInit1

### Design Rationale

Refer to FDD

### Module Outputs

Refer to FDD

#### Per: MotCtrlPrmEstimnPer1

### Design Rationale

Refer to FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

#### Per: MotCtrlPrmEstimnPer2

### Design Rationale

Refer to FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Server Runnables

### SetMotPrmNomEol

### Design Rationale

None

### (Processing of function)………

See GetMotPrmNomEol block in FDD

### SetMotPrmNomEol

### Design Rationale

None

### (Processing of function)………

See SetMotPrmNomEol block in FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

CurrMeasLoaMtgtnEna and FetLoaMtgtnEna are terminated. These flags need not be computed at all.

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

| 1 | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | EA4 Software Naming Conventions | 01.01.00 |

| 4 | Software Design and Coding Standards | 2.1 |

| 5 | FDD – SF102A Motor Control Parameter Estimation | See Synergy subproject version |
