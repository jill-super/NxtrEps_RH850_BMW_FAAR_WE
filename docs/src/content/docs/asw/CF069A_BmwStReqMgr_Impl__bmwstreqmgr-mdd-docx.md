---
title: 'CF069A_BmwStReqMgr_Impl — BmwStReqMgr_MDD'
description: 'Converted Word (.docx) document BmwStReqMgr_MDD.docx from module CF069A_BmwStReqMgr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwStReqMgr_MDD.docx` (Word (.docx), 177 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

BmwStReqMgr

May 22, 2018

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krzysztof Byrski | 1 | 24-Oct-2017 |

| Update to FDD 2.0.0 | Mateusz Bartocha | 2 | 14-Nov-17 |

| Updated Diagram | Matthew Leser | 3 | 10-Jan-18 |

| Updated TargetECUState function inputs | Matthew Leser | 4 | 23-Feb-18 |

| Updated local functions | Krzysztof Byrski | 5 | 22-Mar-2018 |

| Update to FDD 4.0.0 | Krzysztof Byrski | 6 | 22-May-2018 |



Table of Contents1Introduction4

1.1Purpose4

1.2Scope4

2BmwStReqMgr & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwStReqMgr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwStReqMgrInit18

5.1.2Per: BmwStReqMgrPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1Local Function Override9

5.4.2Local Function CalcOfStsSteerAssiAndEpsFctSts9

5.4.3Local Function StsDrvrActvyTmr10

5.4.4Local Function AssiOnToOffFlg10

5.4.5Local Function AllwToOff11

5.4.6Local Function TargetECUState11

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

Module Design Document for CF069A_BmwStReqMgr_Impl

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwStReqMgr & High-Level Description

This function will be responsible for requesting transitions between the states and modes of the steering system based on vehicle signals.

## Design details of software module

### Graphical representation of BmwStReqMgr

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

| - |  |  |  |



*Refer FDD for local constants

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwStReqMgrInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwStReqMgrPer1

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

#### Local Function Override



| Function Name | Override | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwVehCdnVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |

| Return Value | BmwVehCdnVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block Override

#### Local Function CalcOfStsSteerAssiAndEpsFctSts



| Function Name | CalcOfStsSteerAssiAndEpsFctSts | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SysSt_Cnt_T_enum | enum | 0 | 3 |

|  | ThermRednFac_Uls_T_f32 | float32 | 0 | 1 |

|  | RcvrlFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | DiagcStsNonRcvrlReqDiFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | PwrLimrRednFac_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | StsSteerAssi_Cnt_T_enum | enum | 0 | 1 |

|  | BmwEpsFctSts_Cnt_T_enum | enum | 96 | 224 |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block DeterminationOfStatusSteeringAssistAndEpsFctSts

#### Local Function StsDrvrActvyTmr



| Function Name | StsDrvrActvyTmr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | StsDrvrActvy_Cnt_T_enum | enum | 0 | 1 |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block StsDrvrActvyTmr

#### Local Function AssiOnToOffFlg



| Function Name | AssiOnToOffFlg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsNonRcvrlReqDiFltPrsnt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwVehCdnVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwVehSpdSts_Cnt_T_enum | enum | 1 | 15 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 350 |

|  | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |

|  | StsDrvrActvy_Cnt_T_enum | enum | 0 | 1 |

| Return Value | AssiOnToOffFlg_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block AssiOnToOffFlg

#### Local Function AllwToOff



| Function Name | AllwToOff | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |

|  | IgnLine_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | AllwToOff_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block AllwToOff

#### Local Function TargetECUState



| Function Name | TargetECUState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsNonRcvrlReqDiFltPrsnt_Cnt_T_logl | enum | FALSE | TRUE |

|  | BmwVehCdn_Cnt_T_enum | enum | 1 | 15 |

|  | AssiOnToOffFlg_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwTranToDi_Cnt_T_logl | boolean | FALSE | TRUE |

|  | IgnLine_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AllwToOff_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | TarEcuSt_Cnt_T_enum | enum | 0 | 3 |

|  | PwrSplyEnaReq_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysStReqEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysOperMotTqCmdSca_Uls_T_f32 | float | 0 | 1 |



#### Design Rationale

Refer FDD

#### Processing

Implementation of Simulink block TargetECUState

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

## Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document. (See references) |



## Glossary

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



## References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.4.0 R4.0 Rev 3 |

| 2 | MDD Guideline EA4 | 1.02 |

| 3 | EA4 Software Naming Conventions | 1.01 |

| 4 | Software Design and Coding Standards | 2.01 |

| 5 | CF069A_BmwStReqMgr_Design | See Synergy Sub Project Version |
