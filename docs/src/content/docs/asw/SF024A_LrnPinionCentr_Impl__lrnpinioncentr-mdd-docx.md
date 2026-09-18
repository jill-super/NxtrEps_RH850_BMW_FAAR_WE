---
title: 'SF024A_LrnPinionCentr_Impl — LrnPinionCentr_MDD'
description: 'Converted Word (.docx) document LrnPinionCentr_MDD.docx from module SF024A_LrnPinionCentr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `LrnPinionCentr_MDD.docx` (Word (.docx), 145 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

LrnPinionCentr

12-Jan-2018

Prepared By:

Brendon Binder,

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | ML | 1.0 | 18-Sep-2017 |

| Updated DaVinci graphic for Cal name change | BRB | 2.0 | 12-Jan-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2LrnPinionCentr & High-Level Description6

3Design details of software module7

3.1Graphical representation of LrnPinionCentr7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: LrnPinionCentrInit19

5.1.1.1Design Rationale9

5.1.2Per: LrnPinionCentrPer19

5.1.2.1Design Rationale9

5.2Server Runnable9

5.2.1SetInpPrm9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Description9

5.4.2Local Function #29

5.4.2.1Description10

5.4.3Local Function #310

5.4.3.1Description10

5.4.4Local Function #410

5.4.4.1Description10

5.4.5Local Function #510

5.4.5.1Description11

5.4.6Local Function #611

5.4.6.1Description11

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## LrnPinionCentr & High-Level Description

Refer FDD.

## Design details of software module

### Graphical representation of LrnPinionCentr

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

| Refer DataDict.m file from FDD for other constants | - | - | - |



## Software Component Implementation

### Sub-Module Functions

### Init: LrnPinionCentrInit1

Refer FDD Simulink model

### Design Rationale

Refer to Anomaly EA4#17174. Implementation deviates to fix this issue for build.

### Per: LrnPinionCentrPer1

Refer FDD Simulink Model

### Design Rationale

None

### Server Runnable

#### SetInpPrm

Refer FDD Simulink Model

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | RunMinMax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | PinionCentrLrnEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | *MaxHwPosn_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | *MinHwPosn_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘Running MinMax’ function.

### Local Function #2



| Function Name | PosAgVelStCtrl1 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350.0 | 1350.0 |

|  | TarMotVel_MotRadPerSec_T_f32 | float32 | 0.0 | 1600.0 |

|  | *PinionCentrLrnSt_Cnt_T_u08 | uint8 | 0 | 7 |

|  | *TqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *MotPosnCmd_MotRad_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘POSANGVEL State Control 1’ function.

### Local Function #3



| Function Name | PosMotTqStCtrl2 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | *PinionCentrLrnSt_Cnt_T_u08 | uint8 | 0 | 7 |

|  | *TqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *MotPosnCmd_MotRad_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘POSMTRTRQ State Control 2’ function.

### Local Function #4



| Function Name | NegAgVelStCtrl3 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350.0 | 1350.0 |

|  | TarMotVel_MotRadPerSec_T_f32 | float32 | 0.0 | 1600.0 |

|  | *PinionCentrLrnSt_Cnt_T_u08 | uint8 | 0 | 7 |

|  | *TqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *MotPosnCmd_MotRad_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘NEGANGVEL State Control 3’ function.

### Local Function #5



| Function Name | NegMotTqStCtrl4 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MaxHwPosn_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | MinHwPosn_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | *PinionCentrLrnSt_Cnt_T_u08 | uint8 | 0 | 7 |

|  | *TqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *MotPosnCmd_MotRad_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘NEGMTRTRQ State Control 4’ function.

### Local Function #6



| Function Name | MoveToStCtrl5 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | TarHwAg_HwDeg_T_f32 | float32 | -1440.0 | 1440.0 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350.0 | 1350.0 |

|  | TarMotVel_MotRadPerSec_T_f32 | float32 | 0.0 | 1600.0 |

|  | *PinionCentrLrnSt_Cnt_T_u08 | uint8 | 0 | 7 |

|  | *TqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *MotPosnCmd_MotRad_T_f32 | float32 | -1440.0 | 1440.0 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘MOVETO State Control 5’ function.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

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

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.4.0 R4.0 Rev 3 |

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.01 |

| 5 | FDD – SF024A_LrnPinionCentr_Design | See Synergy Subproject verison |
