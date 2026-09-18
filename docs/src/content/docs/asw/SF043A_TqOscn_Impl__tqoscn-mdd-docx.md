---
title: 'SF043A_TqOscn_Impl — TqOscn_MDD'
description: 'Converted Word (.docx) document TqOscn_MDD.docx from module SF043A_TqOscn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `TqOscn_MDD.docx` (Word (.docx), 115 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

TqOscn

Feb 05, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Kanth Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | 1.0 | 05-Feb-2016 |

| Corrected ranges in local function #1 | Krishna Kanth Anne | 2.0 | 25-May-2016 |



Table of Contents

1Introduction5

1.1Purpose5

2TqOscn & High-Level Description6

3Design details of software module7

3.1Graphical representation of TqOscn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: TqOscnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2None9

5.1.3Per: TqOscnPer19

5.1.3.1Design Rationale9

5.1.3.2Store Module Inputs to Local copies9

5.1.3.3(Processing of function)………9

5.1.3.4Store Local copy of outputs into Module Outputs9

5.2Server Runnables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.2Local Function #210

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

## TqOscn & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of TqOscn

### Data Flow Diagram

Please refer FDD

#### Component level DFD

Please refer FDD

#### Function level DFD

Please refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: TqOscnInit1

### Design Rationale

None

### Module Outputs

### None

### Per: TqOscnPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | AmpRateLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LimdAmp_MotNwtMtr_T_f32 | Float32 | 0.0F | 1.2F |

|  | HwOscnRisngRampRate_MotNwtMtrPerSec_T_f32 | Float32 | 0.1F | 4400.0F |

|  | HwOscnFallRampRate_MotNwtMtrPerSec_T_f32 | Float32 | -4400.0F | -0.1F |

|  | HwOscnEna_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | *NonZeroAmpFlg_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | RateLimdAmp_MotNwtMtr_T_f32 | Float32 | 0.0F | 1.2F |



### Local Function #2



| Function Name | ChkFlg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PhaAg_MatRad_T_f32 | Float32 | 0.125F | 0.628F |

| Return Value | TqOscnPhaAg_MatRad_T_f32 | Float32 | 0.0F | 0.628F |



### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None.

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

| 5 | FDD: SF043A_ TqOscn_Design | See Synergy sub project version |
