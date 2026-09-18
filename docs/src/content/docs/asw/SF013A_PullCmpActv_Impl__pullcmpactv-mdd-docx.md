---
title: 'SF013A_PullCmpActv_Impl — PullCmpActv_MDD'
description: 'Converted Word (.docx) document PullCmpActv_MDD.docx from module SF013A_PullCmpActv_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PullCmpActv_MDD.docx` (Word (.docx), 135 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

Active Pull Compensation

Jan 17, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Akhil Krishna N D | 1.0 | 16-Oct-2015 |

| 2 | Updated to FDD version SF013A_PullCmpActv_Design_1.4.0 | SB | 2.0 | 29-Feb-2016 |

| 3 | Updated to design version SF013A_PullCmpActv_Design_1.6.0 | SN | 3.0 | 20-Jun-2016 |

| 4 | Updated to design version 2.0.0 | ML | 4.0 | 17-Jan-2017 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2Active Pull Compensation & High-Level Description6

3Design details of software module7

3.1Graphical representation of Active Pull Compensation7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: PullCmpActvInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: PullCmpActvPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.1.3Per: PullCmpActvPer210

5.1.3.1Design Rationale10

5.1.3.2Store Module Inputs to Local copies10

5.1.3.3(Processing of function)………10

5.1.3.4Store Local copy of outputs into Module Outputs10

5.2Server Runnables11

5.2.1GetPullCmpPrm11

5.2.1.1Design Rationale11

5.2.1.2(Processing of function)………11

5.2.2RstPullCmp11

5.2.2.1Design Rationale11

5.2.2.2(Processing of function)………11

5.2.3SetPullCmpLongTerm11

5.2.3.1Design Rationale11

5.2.3.2(Processing of function)………11

5.2.4SetPullCmpShoTerm11

5.2.4.1Design Rationale11

5.2.4.2(Processing of function)………11

5.3Interrupt Functions11

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Design Rationale12

5.4.1.2Processing12

5.4.2Local Function #212

5.4.2.1Design Rationale12

5.4.2.2Processing12

5.4.3Local Function #112

5.4.3.1Design Rationale13

5.4.3.2Processing13

5.5GLOBAL Function/Macro Definitions13

5.5.1GLOBAL Function #113

5.5.1.1Design Rationale13

5.5.1.2processing13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Active Pull Compensation & High-Level Description

The Active Pull Compensation Function corrects vehicle pull issues by compensating for HW torque offsets detected by the steering system.  These torque offsets are classified as short-term and long-term, each of which is compensated for independently by the algorithm.  When the compensation is applied, the need for the driver to provide a constant input torque to counter these offsets is greatly reduced.

## Design details of software module

### Graphical representation of Active Pull Compensation

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: PullCmpActvInit1

### Design Rationale

None

### Module Outputs

None

### Per: PullCmpActvPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Per: PullCmpActvPer2

### Design Rationale

Please refer FDD.

### Store Module Inputs to Local copies

Please refer FDD and design rationale noted above.

### (Processing of function)………

Please refer FDD.

### Store Local copy of outputs into Module Outputs

None

### Server Runnables

### GetPullCmpPrm

### Design Rationale

None

### (Processing of function)………

See GetPullCmpPrm block in FDD

### RstPullCmp

### Design Rationale

None

### (Processing of function)………

See RstPullCmp block in FDD

### SetPullCmpLongTerm

### Design Rationale

None

### (Processing of function)………

See SetPullCmpLongTerm block in FDD

### SetPullCmpShoTerm

### Design Rationale

None

### (Processing of function)………

See SetPullCmpShoTerm block in FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | ActvCmpEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PullCmpActvShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AbslHwTqFild_HwNwtMtr_T_f32 | float32 | 0.0 | 10.0 |

|  | AbslHwAg_HwDeg_T_f32 | float32 | 0.0 | 1440.0 |

|  | AbslVehYawRateFild_VehDegPerSec_T_f32 | float32 | 0.0 | 128.0 |

|  | AbslVehLatA_MtrPerSecSqd_T_f32 | float32 | 0.0 | 10.0 |

|  | PinionAgConf_Uls_T_f32 | float32 | 0.0 | 1.0 |

|  | VehSpd_Kph_T_f32 | float32 | 0.0 | 511.0 |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AbslHwVel_HwRadPerSec_T_f32 | float32 | 0.0 | 42.0 |

|  | PullCmpCustLrngDi_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehYawRateVld_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | LrngEnad_Cnt_T_logl | boolean | FALSE | TRUE |



### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “ActvCmpEna” block of the Simulink model of the design.

### Local Function #2



| Function Name | CalcIntgrGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10.0 | 10.0 |

|  | PullCmpShoTermPrev_HwNwtMtr_T_f32 | float32 | -10.0 | 10.0 |

| Return Value | IntgtrGainShoTerm_Uls_T_f32 | float32 | 0.0 | 1.0 |



### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “CalcIntgtrGain” block of the Simulink model of the design

### Local Function #3



| Function Name | ErrIntgtrActvLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PullCmpActvShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

|  | IntgtrGainShoTerm_Uls_T_f32 | float32 | 0.0 | 1.0 |

|  | PullErrShoTerm_HwNwtMtr_T_f32 | float32 | -10.0 | 10.0 |

|  | PullCmpShoTermPrev_HwNwtMtr_T_f32 | float32 | -10.0 | 10.0 |

|  | RampDwnStepSize_HwNwtMtr_T_f32 | float32 | 0.0 | 0.6 |

|  | ShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | PullCmpShoTerm_HwNwtMtr_T_f32 | float32 | -10.0 | 10.0 |



### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “ErrIntgtr&ActvLim” block of the Simulink model of the design.

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

None

### Design Rationale

### processing

(Place flowchart/design for local function)

## Known Limitations with Design

None.

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

| 2 | MDD Guideline | Process release 04.02.01 |

| 3 | Software Naming Conve
