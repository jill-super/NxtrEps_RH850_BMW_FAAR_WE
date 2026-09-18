---
title: 'CF071A_BmwHwAgArbnAndEotPosn_Impl — BmwHwAgArbnAndEotPosn_MDD'
description: 'Converted Word (.docx) document BmwHwAgArbnAndEotPosn_MDD.docx from module CF071A_BmwHwAgArbnAndEotPosn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwHwAgArbnAndEotPosn_MDD.docx` (Word (.docx), 191 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

BmwHwAgArbnAndEotPosn

12-Jul-2018

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krzysztof Byrski | 1 | 25-Oct-2017 |

| Updated Local Functions arguments | Krzysztof Byrski | 2 | 08-Nov-2017 |

| Updated Diagram and Function Inputs | Matthew Leser | 3 | 16-Jan-2018 |

| Updated to Design version 3.0.0 | Krzysztof Byrski | 4 | 15-Mar-2018 |

| Updated to Design version 5.1.0 | Marek Brykczyński | 5 | 29-Jun-2018 |

| Updated graphic to include 2 new inputs, modified and added functions | Shawn Penning | 6 | 12-Jul-2018 |



Table of Contents

T

1Introduction5

1.1Purpose5

1.2Scope5

2BmwHwAgArbnAndEotPosn & High-Level Description6

3Design details of software module7

3.1Graphical representation of BmwHwAgArbnAndEotPosn7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: BmwHwAgArbnAndEotPosnInit110

5.1.2Per: BmwHwAgArbnAndEotPosnPer110

5.2Server Runables11

5.2.1ClrBmwRackCentrToVehCentrOffs_Oper11

5.2.2ClrVehCentrPosn_Oper11

5.2.3SetVehCentrPosn_Oper11

5.3Interrupt Functions11

5.4Module Internal (Local) Functions12

5.4.1HwAgSnsrNotTrimNTC12

5.4.2HwPosnFltDetn12

5.4.3PinionAgFltTmr12

5.4.4OffsCorrnTmr13

5.4.5InitTmr13

5.4.6CalcBmwMotAgOffsSelnSt13

5.4.7CalcBmwMotAgOffsSelnStOffsCmpd14

5.4.8CalcBmwMotAgOffsSelnStSubVal14

5.4.9CalcBmwMotAgOffsSelnStTmpCmpd14

5.4.10CalcBmwMotAgOffsSelnStOffsCorrn15

5.4.11CalcBmwMotAgOffsSelnStSigInvld15

5.4.12CalcBmwMotAgOffsSelnStIni15

5.4.13BmwMotAgOffsSelnStTranCase16

5.4.14ChkNrcvrlFlt16

5.4.15TurnCntrCorrlnStsTmr16

5.4.16ChkTurnCntrCorrlnStsCdn16

5.4.17ProcessBmwQuadRotorOffs116

5.4.18ProcessBmwQuadRotorOffs217

5.4.20ProcessBmwQuadOffsSts17

5.4.21ActvtLpFil17

5.4.22CalcBmwPinionAgOffs17

5.4.23BmwMotAgSelnStOffsCmpd18

5.4.24BmwMotAgSelnStSigInvld19

5.4.25PinionAgCalc19

5.4.26ClrNotCmplPinionAgFlg19

5.4.27CalcEot20

5.4.28SetBmwRackCentrToVehCentrOffs20

5.4.29HndlgNTC21

5.5GLOBAL Function/Macro Definitions22

6Known Limitations with Design23

7UNIT TEST CONSIDERATION24

Appendix AAbbreviations and Acronyms25

Appendix BGlossary26

Appendix CReferences27

## Introduction

### Purpose

Module Design Document for CF071A_BmwHwAgArbnAndEotPosn_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwHwAgArbnAndEotPosn & High-Level Description

This function will be responsible for determining the hand wheel position using the motor position to provide an estimate of the hand wheel position.

## Design details of software module

### Graphical representation of BmwHwAgArbnAndEotPosn

### Data Flow Diagram

Refer FDD

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

None

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwHwAgArbnAndEotPosnInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwHwAgArbnAndEotPosnPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

#### ClrBmwRackCentrToVehCentrOffs_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### ClrVehCentrPosn_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

#### SetVehCentrPosn_Oper

#### Design Rationale

Refer FDD

#### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

#### HwAgSnsrNotTrimNTC



| Function Name | HwAgSnsrNotTrimNTC | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | HwAgSnsrNotTrimFlt_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### HwPosnFltDetn



| Function Name | HwPosnFltDetn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwAgSnsrNotTrimFlt_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | PinionAgFltTmrElpd_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### PinionAgFltTmr



| Function Name | PinionAgFltTmr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAgSnsrNotTrimFlt_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | PinionAgFltTmrElpd_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### OffsCorrnTmr



| Function Name | OffsCorrnTmr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | OffsCorrnTmrElpd_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### InitTmr



| Function Name | InitTmr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | AllwExitFromInit_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcBmwMotAgOffsSelnSt



| Function Name | CalcBmwMotAgOffsSelnSt | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TurnCntrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwQuadOffsSts_Cnt_T_enum | enum | 0 | 15 |

|  | PinionAgFltTmrElpd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | OffsCorrnTmrElpd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwAgNotVldFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwExitFromInit_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcBmwMotAgOffsSelnStOffsCmpd



| Function Name | CalcBmwMotAgOffsSelnStOffsCmpd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TurnCntrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwQuadOffsSts_Cnt_T_enum | enum | 0 | 15 |

|  | HwAgNotVldFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcBmwMotAgOffsSelnStSubVal



| Function Name | CalcBmwMotAgOffsSelnStSubVal | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwQuadOffsSts_Cnt_T_enum | enum | 0 | 15 |

|  | HwAgNotVldFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcBmwMotAgOffsSelnStTmpCmpd



| Function Name | CalcBmwMotAgOffsSelnStTmpCmpd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwQuadOffsSts_Cnt_T_enum | enum | 0 | 15 |

|  | HwAgNotVldFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTran_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### CalcBmwMotAgOffsSelnStOffsCorrn



| Function Name | CalcBmwMotAgOffsSelnStOffsCorrn | Type | Mi

*Body truncated: document is longer than the excerpt shown here.*
