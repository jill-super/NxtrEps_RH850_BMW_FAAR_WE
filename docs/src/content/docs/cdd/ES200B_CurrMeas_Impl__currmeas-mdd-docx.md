---
title: 'ES200B_CurrMeas_Impl — CurrMeas_MDD'
description: 'Converted Word (.docx) document CurrMeas_MDD.docx from module ES200B_CurrMeas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CurrMeas_MDD.docx` (Word (.docx), 169 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

CurrMeas

Mar 23, 2018

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

| Initial Version | Krzysztof Byrski | 1.0 | 19-May-2017 |

| Fixed anomaly EA4#13330 by using required NVM blocks as applicable | Krishna Anne | 2.0 | 16-Oct-17 |

| Created local functions for reducing the complexity of OffsetCalibration and GainCalibration functions | Mrudula Paturi | 3.0 | 23-Mar-18 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2CurrMeas & High-Level Description6

3Design details of software module7

3.1Graphical representation of CurrMeas7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: CurrMeasInit19

5.1.2Per: CurrMeasPer19

5.1.3Per: CurrMeasPer29

5.1.4Per: CurrMeasPer310

5.2Server Runables11

5.2.1CurrMeasEolGainReq_Oper11

5.2.2CurrMeasEolGainStsReq_Oper11

5.2.3CurrMeasEolOffsReq_Oper11

5.2.4CurrMeasEolOffsStsReq_Oper11

5.2.5CurrMeasGainReadReqSngIvtr_Oper11

5.2.6CurrMeasGainWrReqSngIvtr_Oper11

5.2.7CurrMeasOffsReadReqSngIvtr_Oper12

5.2.8CurrMeasOffsWrReqSngIvtr_Oper12

5.3Interrupt Functions13

5.4Module Internal (Local) Functions13

5.4.1OffsetCalibration13

5.4.2GainCalibration14

5.4.3RangeChkWIABC14

5.4.4ProtocolChkENABC15

5.4.5CalcMotCurrMotAgCorrd15

5.4.6CalMotCurrCorrdABC15

5.4.7OffsCalcABC16

5.5GLOBAL Function/Macro Definitions17

6Known Limitations with Design18

7UNIT TEST CONSIDERATION19

Appendix AAbbreviations and Acronyms20

Appendix BGlossary21

Appendix CReferences22

## Introduction

### Purpose

Module Design Document for ES200B_CurrMeas.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## CurrMeas & High-Level Description

Refer FDD.

## Design details of software module

### Graphical representation of CurrMeas

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

| CALPROCNOTSTRTD_CNT_U08 | 1 | Cnt | 0 |

| CALPROCSTRTD_CNT_U08 | 1 | Cnt | 1 |

| CALPROCPASS_CNT_U08 | 1 | Cnt | 2 |

| CALPROCPHAABCEOLOUTOFRNG_CNT_U08 | 1 | Cnt | 4 |

| CALPROCVEHSPDCNDNOTMET_CNT_U08 | 1 | Cnt | 16 |

| CALPROCMOTVELMRFCNDNOTMET_CNT_U08 | 1 | Cnt | 64 |

| VEHSPDCDNNOTMET_CNT_U08 | 1 | Cnt | 4 |

| MOTVELMRFCDNNOTMET_CNT_U08 | 1 | Cnt | 8 |

| DIAGCSTSINVTRINACTV_CNT_U08 | 1 | Cnt | 16 |

| FAILDATENA_CNT_U08 | 1 | Cnt | 2 |

| FAILDATWRMININ_CNT_U08 | 1 | Cnt | 3 |

| INVTRINACTV_CNT_U08 | 1 | Cnt | 8 |

| DIFOFFSRNGCHKMAX_VOLT_F32 | Single precision float | Volt | 1.0 |

| DEGREES30_MOTRAD_F32 | Single precision float | MotRad | 0.5236 |

| MAXCURRCORRD_AMPR_F32 | Single precision float | Ampr | 200.0 |

| PHAONTIBCOK_CNT_U08 | 1 | Cnt | 0x03 |

| PHAONTIACOK_CNT_U08 | 1 | Cnt | 0x05 |

| PHAONTIABOK_CNT_U08 | 1 | Cnt | 0x06 |

| PHAONTIABCOK_CNT_U08 | 1 | Cnt | 0x07 |

| PHAONTIA_CNT_U08 | 1 | Cnt | 0x04 |

| PHAONTIB_CNT_U08 | 1 | Cnt | 0x02 |

| PHAONTIC_CNT_U08 | 1 | Cnt | 0x01 |

| NANOSECTOSEC_ULS_F32 | Single precision float | Uls | 0.000000001 |



## Software Component Implementation

### Sub-Module Functions

#### Init: CurrMeasInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: CurrMeasPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

#### Per: CurrMeasPer2

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

#### Per: CurrMeasPer3

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

#### CurrMeasEolGainReq_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasEolGainStsReq_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasEolOffsReq_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasEolOffsStsReq_Oper

#### Design Rationale

Refer FDD

#### CurrMeasGainReadReqSngIvtr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasGainWrReqSngIvtr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasOffsReadReqSngIvtr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### CurrMeasOffsWrReqSngIvtr_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

#### OffsetCalibration



| Function Name | OffsetCalibration | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrAdcVlyA_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyB_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyC_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotVelMrf_MotRadPerSec_T_f32 | float32 | -1350.0 | 1350.0 |

|  | VehSpd_Kph_T_f32 | float32 | 0.0 | 511.0 |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BrdgVltg_Volt_T_f32 | float32 | 6.0 | 26.5 |

|  | DiagcStsIvtr1Inactv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | N/A | - | - | - |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### GainCalibration



| Function Name | GainCalibration | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrEolOffsProcFlg_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotCurrAdcVlyA_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyB_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyC_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotVelMrf_MotRadPerSec_T_f32 | float32 | -1350.0 | 1350.0 |

|  | MotCurrOffsZeroAvrgA_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrOffsZeroAvrgB_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrOffsZeroAvrgC_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | VehSpd_Kph_T_f32 | float32 | 0.0 | 511.0 |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | DiagcStsIvtr1Inactv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | MotCurrEolCalStPrev_Cnt_T_enum | MotCurrEolCalSt2 | 0 | 8 |

| Return Value | N/A | - | - | - |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### RangeChkWIABC



| Function Name | RangeChkWIABC | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrAdcVlyA_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyB_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | MotCurrAdcVlyC_Volt_T_f32 | float32 | 0.0 | 5.0 |

| Return Value | InRng_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### ProtocolChkENABC



| Function Name | ProtocolChkENABC | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A | - | - | - |

| Return Value | ProtocolChkEn_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcMotCurrMotAgCorrd



| Function Name | CalcMotCurrMotAgCorrd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A | - | - | - |

| Return Value | MotCtrlCurrMeasMotAgCorrd

*Body truncated: document is longer than the excerpt shown here.*
