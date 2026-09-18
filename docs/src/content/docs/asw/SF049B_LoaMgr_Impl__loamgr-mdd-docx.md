---
title: 'SF049B_LoaMgr_Impl — LoaMgr_MDD'
description: 'Converted Word (.docx) document LoaMgr_MDD.docx from module SF049B_LoaMgr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `LoaMgr_MDD.docx` (Word (.docx), 119 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

LoaMgr

October 6, 2017

Prepared By:

Matthew Leser

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Matthew Leser | 1 | 06-Oct-2017 |



Table of Contents1Introduction5

1.1Purpose5

2LoaMgr High-Level Description6

3Design details of software module7

3.1Graphical representation of LoaMgr7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: LoaMgrInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: LoaMgrPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing11

5.4.2Local Function #211

5.4.2.1Design Rationale11

5.4.2.2Processing11

5.4.3Local Function #311

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.4Local Function #411

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Local Function #512

5.4.5.1Design Rationale12

5.4.5.2Processing12

5.4.6Local Function #612

5.4.6.1Design Rationale12

5.4.6.2Processing12

5.4.7Local Function #712

5.4.7.1Design Rationale12

5.4.7.2Processing13

5.4.8Local Function #813

5.4.8.1Design Rationale13

5.4.8.2Processing13

5.5GLOBAL Function/Macro Definitions13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Introduction

### Purpose

MDD for Loss of Assist Manager

## LoaMgr High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of LoaMgr

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: LoaMgrInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: LoaMgrPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | LtchInp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IdptSig_Cnt_T_u08 | uint8 | 0 | 4 |

|  | MaxAllwdVal_Cnt_T_u08 | uint8 | 2 | 4 |

|  | *PrevVal_Cnt_T_u08 | uint8 | 0 | 4 |

| Return Value | HwTqResp_Cnt_T_u08 | uint8 | 0 | 4 |



### Design Rationale

None

### Processing

Refer to ‘Latch_Inputs’ block in FDD at ‘SF049B_LoaMgr/LoaMgr/LoaMgrPer1/Latch_Inputs’

### Local Function #2



| Function Name | CntMtgtnReq | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | MotAgLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | CurrMeasLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | IvtrLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | MultiMtgtnResp_Cnt_T_u08 | uint8 | 0 | 3 |



### Design Rationale

None

### Processing

Refer to ‘CntMtgtnReq’ block in FDD at ‘SF049B_LoaMgr/LoaMgr/LoaMgrPer1/Arbitrate_Responses/CntSwBasdMtgtn/CntMtgtnReq’

### Local Function #3



| Function Name | ReqHwTqResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqIdptMin_Cnt_T_u08 | uint8 | 0 | 4 |

|  | TqLoaAvl_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | HwTqResp_Cnt_T_u08 | uint8 | 0 | 5 |



### Design Rationale

None

### Processing

Refer to ‘HwTqResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #4



| Function Name | ReqMotAgResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgIdptMin_Cnt_T_u08 | uint8 | 0 | 3 |

|  | MotAgSnsrlsAvl_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | MotAgResp_Cnt_T_u08 | uint8 | 0 | 5 |



### Design Rationale

None

### Processing

Refer to ‘MotAgResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #5



| Function Name | ReqCurrMeasResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CurrMeasIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | CurrMeasResp_Cnt_T_u08 | uint8 | 0 | 5 |



### Design Rationale

None

### Processing

Refer to ‘CurrMeasResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #6



| Function Name | ReqInvtrResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IvtrIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | InvtrResp_Cnt_T_u08 | uint8 | 0 | 5 |



### Design Rationale

None

### Processing

Refer to ‘CurrMeasResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #7



| Function Name | CntSwBasdMtgtnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Resp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | PrevMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | MtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |



### Design Rationale

None

### Processing

This function corresponds to common logic (for all requests) in ‘CntSwBasdMtgtn’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Arbitrate_Responses’

### Local Function #8



| Function Name | SelFinalResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MultiMtgtnResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | HwTqResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | MotAgResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | CurrMeasResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | InvtrResp_Cnt_T_u08 | uint8 | 0 | 5 |

| Return Value | LoaSt_Cnt_T_enum | LoaSt1 | 0 | 5 |



### Design Rationale

None

### Processing

This function corresponds to ‘SelFinalResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Arbitrate_Responses’

### Local Function #9



| Function Name | SetFaults | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LoaSt_Cnt_T_enum | LoaSt1 | 0 | 5 |

|  | HwTqIdptMin_Cnt_T_u08 | uint8 | 0 | 4 |

|  | MotAgIdptMin_Cnt_T_u08 | uint8 | 0 | 3 |

|  | CurrMeasIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

|  | IvtrIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | None |  |  |  |



### Design Rationale

None

### Processing

This function corresponds to ‘Set_Faults’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1’

### Local Function #10



| Function Name | SwMtgtnEn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | MotAgLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | CurrMeasLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | IvtrLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | VehSpeedMod_Cnt_T_enum | enum | STEERMOD_BASEPS | STEERMOD_FULLYATNMS |

|  | *LoaSca_Uls_T_f32 | float32 | 0 | 1 |

|  | *LoaRateLim_UlsPerSec_T_f32 | float32 | 0.01 | 500 |

| Return Value | None |  |  |  |



### Design Rationale

None

### Processing

This function corresponds to ‘SwMtgtn’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Assign_Scale’.

Note that ‘*LoaSca_Uls_T_f32’ and ‘*LoaRateLim_UlsPerSec_T_f32’ are the outputs of this function.

### Local Function #11

### Design Rationale

None

### Processing

This function corresponds to ‘coder block in FDD at ‘SF049B_LoaMgr/LoaMgr/LoaMgrPer1/coder’ .

### GLOBAL Function/Macro Definitions

None

## Known Limitation

*Body truncated: document is longer than the excerpt shown here.*
