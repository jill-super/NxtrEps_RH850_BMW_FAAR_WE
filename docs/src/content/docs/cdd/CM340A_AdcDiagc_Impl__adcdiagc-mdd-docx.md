---
title: 'CM340A_AdcDiagc_Impl — AdcDiagc_MDD'
description: 'Converted Word (.docx) document AdcDiagc_MDD.docx from module CM340A_AdcDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `AdcDiagc_MDD.docx` (Word (.docx), 160 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

AdcDiagc

Mar 13, 2017

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

| Initial Version | Rijvi Ahmed | 1.0 | 02-Feb-2016 |

| Updated per design rev. 1.1.0 | Rijvi Ahmed | 2.0 | 23-Mar-2016 |

| Updated per design rev. 1.4.0 | Avinash James | 3.0 | 21-Jun-2016 |

| Updated per design rev. 1.6.0 | Avinash James | 4.0 | 15-Jul-2016 |

| Updated per design rev. 1.7.0 | Avinash James | 5.0 | 25-Aug-2016 |

| Updated to include error injection | Avinash James | 6.0 | 13-Mar-2017 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2AdcDiagc & High-Level Description6

3Design details of software module7

3.1Graphical representation of AdcDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: AdcDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: AdcDiagcPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #210

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.4.3Local Function #310

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.4Local Function #411

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Local Function #511

5.4.5.1Design Rationale11

5.4.5.2Processing11

5.4.6Local Function #611

5.4.6.1Design Rationale12

5.4.6.2Processing12

5.4.7Local Function #712

5.4.7.1Design Rationale12

5.4.7.2Processing12

5.4.8Local Function #812

5.4.8.1Design Rationale12

5.4.8.2Processing12

5.4.9Local Function #912

5.4.9.1Design Rationale12

5.4.9.2Processing12

5.5GLOBAL Function/Macro Definitions13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Introduction

### Purpose

MDD for AdcDiagc

### Scope

## AdcDiagc & High-Level Description

Refer to FDD.

## Design details of software module

### Graphical representation of AdcDiagc

### Data Flow Diagram

None.

#### Component level DFD

Refer FDD.

#### Function level DFD

Refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MAXADCDIAGCST_CNT_U08 | 1 | CNT | 7U |

| Refer to the FDD |  |  |  |

| MASKFLTCNTR_CNT_U08 | 1 | CNT | 127U |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: AdcDiagcInit1

### Design Rationale

None

### Module Outputs

None

#### Per: AdcDiagcPer1

### Design Rationale

Refer FDD.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD.

### Server Runables

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | St2Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | *RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |



### Design Rationale

### Processing

See “State 2” block in the Simulink model of the design.

### Local Function #2



| Function Name | St4Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | *RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |



### Design Rationale

### Processing

See “State 4” block in the Simulink model of the design.

### Local Function #3



| Function Name | St6Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | *RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |



### Design Rationale

### Processing

See “State 6” block in the Simulink model of the design.

### Local Function #4



| Function Name | St0Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | *RollgCntr_Cnt_T_u08 | *uint8 | 00 | 3255 |

|  |  | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |



### Design Rationale

### Processing

See “State 0” block in the Simulink model of the design.

### Local Function #5



| Function Name | Adc0StBasdProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Adc0ParFlt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | None | N/A | N/A | N/A |



### Design Rationale

### Processing

See “Adc0 State Based Processing” block in the Simulink model of the design.

### Local Function #6



| Function Name | Adc1StBasdProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Adc1ParFlt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | None | N/A | N/A | N/A |



### Design Rationale

### Processing

See “Adc1 State Based Processing” block in the Simulink model of the design.

### Local Function #7



| Function Name | AdcDiagcPtrProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | N/A | N/A | N/A |

| Return Value | None | N/A | N/A | N/A |



### Design Rationale

### Processing

See “Adc Daigc Pointer” block in the Simulink model of the design.

### Local Function #8



| Function Name | ScanGroupAccrcyChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcScanGroupInpRefVltg_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcScanGroupRefVltg_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcScanGroupInpRefPrm_Cnt_T_u08 | Uint8 | 0 | 255 |

| Return Value | ScanGroupAccrcyChkRefPrm_Cnt_u08 | Uint8 | 0 | 255 |



### Design Rationale

### Processing

See “Scan Group Accuracy Check” block in the Simulink model of the design.

### Local Function #9



| Function Name | SetAdcParFlt | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | *Adc0ParFlt_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | *Adc1ParFlt_Cnt_T_u08 | Uint8 | 0 | 255 |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

See “Adc Parity Fault” block in the Simulink model of the design.

### GLOBAL Function/Macro Definitions

Note: The server runnable of this component are non-rte. So they are actually global functions which should belong to this section. But as they are already described under Server Runnable section so it’s omitted here.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

The overflow for the following PIMs are intentional as they are used as rollin

*Body truncated: document is longer than the excerpt shown here.*
