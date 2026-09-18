---
title: 'CF089A_BmwDrvgDynStMac_Impl — BmwDrvgDynStMac_MDD'
description: 'Converted Word (.docx) document BmwDrvgDynStMac_MDD.docx from module CF089A_BmwDrvgDynStMac_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwDrvgDynStMac_MDD.docx` (Word (.docx), 124 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

BmwDrvgDynStMac

April 13, 2018

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

| Initial version | Krzysztof Byrski | 1 | 17-Apr-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2BmwDrvgDynStMac & High-Level Description6

3Design details of software module7

3.1Graphical representation of BmwDrvgDynStMac7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: BmwDrvgDynStMacInit19

5.1.2Per: BmwDrvgDynStMacPer19

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1Local Function DetermineErrorMode10

5.4.2Local Function Fac10

5.4.3Local Function AssiLvlCnd11

5.4.4Local Function CheckActivityTime11

5.4.5Local Function CheckDeactivateTime11

5.4.6Local Function ErrorIfTi12

5.4.7Local Function StateMachine12

5.4.8Local Function StateMachineInit13

5.4.9Local Function StateMachineIfAvl13

5.4.10Local Function StateMachineIfActv14

5.4.11Local Function StateMachineStbEpsSts14

5.4.12Local Function StateMachineEntry15

5.5GLOBAL Function/Macro Definitions16

6Known Limitations with Design17

7UNIT TEST CONSIDERATION18

Appendix AAbbreviations and Acronyms19

Appendix BGlossary20

Appendix CReferences21

## Introduction

### Purpose

Model Deign Document for CF089A_BmwDrvgDynStMac_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwDrvgDynStMac & High-Level Description

The component implements the functionality of Driving Dynamics State Machine. It is based on requirements for DD State Machine in LH10716411 starting from ID_6159. It outputs signals for CF083A and CF040A.

## Design details of software module

### Graphical representation of BmwDrvgDynStMac

### Data Flow Diagram

Refer FDD

#### Component level DFD

None

#### Function level DFD

None

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| * |  |  |  |



*Refer FDD for local constants

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwDrvgDynStMacInit1

#### Design Rationale

Refer FDD

#### Module Outputs

None

#### Per: BmwDrvgDynStMacPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### Local Function DetermineErrorMode



| Function Name | DetermineErrorMode | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SysStFltOutpReqDi_Cnt_T_logl | boolean | 0 | 1 |

|  | DiagcStsNonRcvrlReqDiFltPrsnt_Cnt_T_logl | boolean | 0 | 1 |

|  | DiagcStsCtrldShtDwnFltPrsnt_Cnt_T_logl | boolean | 0 | 1 |

|  | StsSteerAssi_Cnt_T_enum | enum | 0 | 1 |

|  | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |

| Return Value | ErrMod_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "DetermineErrorMode" Simulink block

#### Processing

Refer FDD

#### Local Function Fac



| Function Name | Fac | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EffortCmdSca_Uls_T_f32 | float32 | 1 | 2 |

|  | DampgCmdSca_Uls_T_f32 | float32 | 0 | 1 |

|  | RtnCmdSca_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | Fac_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "Fac" Simulink block

#### Processing

Refer FDD

#### Local Function AssiLvlCnd



| Function Name | AssiLvlCnd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdPwrLimd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | MotTqCmdPwrLimdActvtUppr_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdPwrLimdActvtLowr_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdPwrLimdDeactvtLowr_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "AssiLvlCnd" Simulink block

#### Processing

Refer FDD

#### Local Function CheckActivityTime



| Function Name | CheckActivityTime | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdPwrLimdCdnActvt_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | MotTqCmdPwrLimdActvt_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "CheckActivity Time" Simulink block

#### Processing

Refer FDD

#### Local Function CheckDeactivateTime



| Function Name | CheckDeactivateTime | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdPwrLimdCdnDeactvt_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | MotTqCmdPwrLimdDeactvt_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "CheckDeactivate Time" Simulink block

#### Processing

Refer FDD

#### Local Function ErrorIfTi



| Function Name | ErrorIfTi | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ErrIf_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | ErrIfTi_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "ErrorIfTi" Simulink block

#### Processing

Refer FDD

#### Local Function StateMachine



| Function Name | StateMachine | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ErrMod_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ErrIf_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwTarHwTqOvrlQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwDrvgDynFacQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwTarSteerTqDrvrActrQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwTrfcJamAssiDampgStReq_Cnt_T_enum | enum | 1 | 15 |

|  | Fac_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdOvrlEquZero_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdPwrLimd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | N/A |  |  |  |



#### Design Rationale

Implementation of "StateMachine" Simulink state machine

#### Processing

Refer FDD

#### Local Function StateMachineInit



| Function Name | StateMachineInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ErrMod_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ErrIf_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwTarHwTqOvrlQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwDrvgDynFacQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwTarSteerTqDrvrActrQlfr_Cnt_T_enum | enum | 2 | 15 |

|  | BmwTrfcJamAssiDampgStReq_Cnt_T_enum | enum | 1 | 15 |

|  | MotTqCmdPwrLimdActvtUppr_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotTqCmdPwrLimdActvtLowr_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | N/A |  |  |  |



#### Design Rationale

Implementation of INIT State

#### Processing

Refer FDD

#### Local Function StateMachineIfAvl



| Function Name | StateMachineIfAvl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ErrMod_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ErrIf_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwTarHwTqOvrlQlfr_Cnt_T_

*Body truncated: document is longer than the excerpt shown here.*
