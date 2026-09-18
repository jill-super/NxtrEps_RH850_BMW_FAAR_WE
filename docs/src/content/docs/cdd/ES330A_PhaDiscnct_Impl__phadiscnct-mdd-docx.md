---
title: 'ES330A_PhaDiscnct_Impl — PhaDiscnct_MDD'
description: 'Converted Word (.docx) document PhaDiscnct_MDD.docx from module ES330A_PhaDiscnct_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PhaDiscnct_MDD.docx` (Word (.docx), 122 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

PhaDiscnct

February 16, 2018

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

| Initial Version | Krzysztof Byrski | 1 | 24-Aug-2017 |

| Updated as per Design version 1.2.0 | Krzysztof Byrski | 2 | 03-Oct-2017 |

| Updated as per Design version 1.3.0 | Krzysztof Byrski | 3 | 16-Feb-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2PhaDiscnct & High-Level Description5

3Design details of software module6

3.1Graphical representation of PhaDiscnct6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: PhaDiscnctInit18

5.1.2Per: PhaDiscnctPer18

5.1.3Per: PhaDiscnctPer28

5.2Server Runables8

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function PerformDiag9

5.4.2Local Function ClosingStateBody9

5.4.3Local Function ClosedStateBody10

5.4.4Local Function OpeningStateBody10

5.4.5Local Function OpenedStateBody10

5.4.6Local Function SetHwPhaDiscnctIO11

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

MDD for ES330A_PhaDiscnct_Impl

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## PhaDiscnct & High-Level Description

Phase Disconnect provides mechanism of disconnecting Motor Phases from system in order to prevent generation of unintended negative or positive motor torque. Phase Disconnect is controlled by System State and Motor Control Gate Driver FET fault signals. Phase Disconnect functionality provides support for loss of assist mitigation.

## Design details of software module

### Graphical representation of PhaDiscnct

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

| DIAGFLTPRMFAILTODIAGFLG_CNT_U08 | 1 | Cnt | 8 |

| DIAGMOTCURRCORRDABITPOSN_CNT_U08 | 1 | Cnt | 1 |

| DIAGMOTCURRCORRDBBITPOSN_CNT_U08 | 1 | Cnt | 2 |

| DIAGMOTCURRCORRDCBITPOSN_CNT_U08 | 1 | Cnt | 4 |

| DIAGSTCMPL_CNT_U08 | 1 | Cnt | 2 |

| DIAGSTINI_CNT_U08 | 1 | Cnt | 0 |

| DIAGSTPROC_CNT_U08 | 1 | Cnt | 1 |

| DIAGSTSFAILTODIAG_CNT_U08 | 1 | Cnt | 2 |

| DIAGSTSFAILTOOPEN_CNT_U08 | 1 | Cnt | 1 |

| DIAGSTSPASS_CNT_U08 | 1 | Cnt | 0 |

| DIAGTSTITRNPHAA_CNT_U08 | 1 | Cnt | 2 |

| DIAGTSTITRNPHAB_CNT_U08 | 1 | Cnt | 1 |

| DIAGTSTITRNPHAC_CNT_U08 | 1 | Cnt | 0 |

| DISCNCTCURRCOMPIDX_CNT_U08 | 1 | Cnt | 0 |

| OPERSTCLSPROGSN_CNT_U08 | 1 | Cnt | 0 |

| OPERSTCLS_CNT_U08 | 1 | Cnt | 1 |

| OPERSTOPENPROGSN_CNT_U08 | 1 | Cnt | 2 |

| OPERSTOPEN_CNT_U08 | 1 | Cnt | 3 |

| PHADISCNCTCMDALLOFF_CNT_U08 | 1 | Cnt | 0 |

| PHADISCNCTCMDALLON_CNT_U08 | 1 | Cnt | 7 |

| PHADISCNCTCMDAON_CNT_U08 | 1 | Cnt | 1 |

| PHADISCNCTCMDBON_CNT_U08 | 1 | Cnt | 2 |

| PHADISCNCTCMDCON_CNT_U08 | 1 | Cnt | 4 |



## Software Component Implementation

### Sub-Module Functions

#### Init: PhaDiscnctInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: PhaDiscnctPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

Refer FDD

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

#### Per: PhaDiscnctPer2

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

#### Local Function PerformDiag



| Function Name | PerformDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotCurrCorrdA_Ampr_T_f32 | float32 | -200.0 | 200.0 |

|  | MotCurrCorrdB_Ampr_T_f32 | float32 | -200.0 | 200.0 |

|  | MotCurrCorrdC_Ampr_T_f32 | float32 | -200.0 | 200.0 |

| Return Value | PhaDiscnctDiagcPwmVect_Cnt_T_enum | enum | 1 | 4 |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### Local Function ClosingStateBody



| Function Name | ClosingStateBody | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | StrtUpSt_Cnt_T_u08 | uint8 | 0 | 160 |

|  | SysSt_Cnt_T_enum | enum | 0 | 3 |

| Return Value | PhaDiscnctInactvTemp_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### Local Function ClosedStateBody



| Function Name | ClosedStateBody | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IvtrFetFltPha_Cnt_T_enum | enum | 0 | 4 |

|  | IvtrFetFltTyp_Cnt_T_enum | enum | 0 | 4 |

|  | SysSt_Cnt_T_enum | enum | 0 | 3 |

| Return Value | PhaDiscnctCmdTemp_Cnt_T_u08 | Uint8 | 0 | 7 |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### Local Function OpeningStateBody



| Function Name | OpeningStateBody | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IvtrFetFltTyp_Cnt_T_enum | enum | 0 | 4 |

|  | SysSt_Cnt_T_enum | enum | 0 | 3 |

| Return Value | PhaDiscnctCmdTemp_Cnt_T_u08 | uint8 | 0 | 7 |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### Local Function OpenedStateBody



| Function Name | OpenedStateBody | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IvtrFetFltPha_Cnt_T_enum | enum | 0 | 4 |

|  | IvtrFetFltTyp_Cnt_T_enum | enum | 0 | 4 |

|  | SysSt_Cnt_T_enum | enum | 0 | 3 |

| Return Value | PhaDiscnctInactvTemp_Cnt_T_logl | boolean | FALSE | TRUE |

|  | PhaDiscnctCmdTemp_Cnt_T_u08 | uint8 | 0 | 7 |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

#### Local Function SetHwPhaDiscnctIO



| Function Name | SetHwPhaDiscnctIO | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PhaDiscnt_Cnt_T_u08 | uint8 | 0 | 7 |

| Return Value | N/A |  |  |  |



#### Design Rationale

Refer FDD

#### Processing

Refer FDD

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

## Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |



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

| 5 | ES330A_PhaDiscnct_Design | See Synergy Sub Project Version |
