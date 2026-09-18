---
title: 'CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl — BmwTqOvrlCdngAndDrvgDynFac_MDD'
description: 'Converted Word (.docx) document BmwTqOvrlCdngAndDrvgDynFac_MDD.docx from module CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwTqOvrlCdngAndDrvgDynFac_MDD.docx` (Word (.docx), 127 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

BmwTqOvrlCdngAndDrvgDynFac

April 26, 2018

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Tychy, PolandChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial version | Marek Brykczyński | 1 | 26-Apr-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2BmwTqOvrlCdngAndDrvgDynFac & High-Level Description6

3Design details of software module7

3.1Graphical representation of BmwTqOvrlCdngAndDrvgDynFac7

3.2Data Flow Diagram7

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: BmwTqOvrlCdngAndDrvgDynFacInit110

5.1.2Per: BmwTqOvrlCdngAndDrvgDynFacPer110

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions11

5.4.1CalcCdndTqOvrl11

5.4.2CalcnDampgCmdSca11

5.4.3CalcnEffortCmdSca11

5.4.4CalcnLimdCdndTqOvrl11

5.4.5CalcnRtnCmdSca12

5.4.6StTranDetn12

5.4.7TqOvrlCdng12

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Introduction

### Purpose

Module Design Document for CF040A_BmwTqOvrlCdngAndDrvgDynFac_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwTqOvrlCdngAndDrvgDynFac & High-Level Description

The BMW Torque Overlay Conditioning And Driving Dynamic Factor function handles the filtering and ramping of the BMW Output Torque Overlay Command functionality and conditioning of the BMW Driving Dynamic Factors for Effort/Assist, Return and Damping.

## Design details of software module

### Graphical representation of BmwTqOvrlCdngAndDrvgDynFac

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

| - |  |  |  |



Refer FDD for local constants.

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwTqOvrlCdngAndDrvgDynFacInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwTqOvrlCdngAndDrvgDynFacPer1

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

#### CalcCdndTqOvrl



| Function Name | CalcCdndTqOvrl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FildBmwTarSteerTqDrvrActr_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | BmwTarSteerTqDrvrActr_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | BmwDrvgDynErrIfActv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | CdndTqOvrl_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |



#### CalcnDampgCmdSca



| Function Name | CalcnDampgCmdSca | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DrvgDynActv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ReqdDampgCmdSca_Uls_T_f32 | float32 | 0 | 1 |

|  | DrvgDynActvTrig_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | - | - | - | - |



#### CalcnEffortCmdSca



| Function Name | CalcnEffortCmdSca | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DrvgDynActv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ReqdEffortCmdSca_Uls_T_f32 | float32 | 1 | 2 |

|  | DrvgDynActvTrig_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | - | - | - | - |



#### CalcnLimdCdndTqOvrl



| Function Name | CalcnLimdCdndTqOvrl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CdndTqOvrl_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | VehSpd_Kph_T_u9p7 | uint16 | 0 | 68408 |

| Return Value | - | - | - | - |



#### CalcnRtnCmdSca



| Function Name | CalcnRtnCmdSca | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DrvgDynActv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ReqdRtnCmdSca_Uls_T_f32 | float32 | 0 | 1 |

|  | DrvgDynActvTrig_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | - | - | - | - |



#### StTranDetn



| Function Name | StTranDetn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DrvgDynIfSt_Cnt_T_u08 | uint8 | 32 | 255 |

|  | BmwTarSteerTqDrvrActr_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | FildBmwTarSteerTqDrvrActr_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | OutpRstTrig_Cnt_T_logl | boolean | FALSE | TRUE |



#### TqOvrlCdng



| Function Name | TqOvrlCdng | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DrvgDynIfSt_Cnt_T_u08 | uint8 | 32 | 255 |

|  | BmwTarSteerTqDrvrActr_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | VehSpd_Kph_T_u9p7 | uint16 | 0 | 68408 |

|  | BmwDrvgDynErrIfActv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | OutpRstTrig_Cnt_T_logl | boolean | FALSE | TRUE |



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

| 5 | CF011A_BmwTqOvrlCdngAndDrvgDynFac_Design | See Synergy Sub Project Version |
