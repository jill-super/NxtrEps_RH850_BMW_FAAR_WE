---
title: 'CF020A_BmwHaptcFb_Impl — BmwHaptcFb_MDD'
description: 'Converted Word (.docx) document BmwHaptcFb_MDD.docx from module CF020A_BmwHaptcFb_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwHaptcFb_MDD.docx` (Word (.docx), 125 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 9

## Converted content

For

BmwHaptcFb

May 18, 2018

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

| Initial version | Krzysztof Byrski | 1 | 18-May-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2BmwHaptcFb & High-Level Description5

3Design details of software module6

3.1Graphical representation of BmwHaptcFb6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: BmwHaptcFbInit18

5.1.2Per: BmwHaptcFbPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1Local Function CalcBmwHaptcFbPatNr9

5.4.2Local Function CalcBmwHaptcFbIntenNr9

5.4.3Local Function CalcHwOscnEna10

5.4.4Local Function CalcAmpAndFrq10

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

Module Design Document for CF020A_BmwHaptcFb_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwHaptcFb & High-Level Description

This function will alert the driver through handwheel haptic feedback if a lane departure is detected. This function accepts pulse pattern, amplitude, and frequency inputs from the customer and then provides an enable/disable signal.

## Design details of software module

### Graphical representation of BmwHaptcFb

### Data Flow Diagram

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



*Refer FDD for local constants

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: BmwHaptcFbInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: BmwHaptcFbPer1

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

#### Local Function CalcBmwHaptcFbPatNr



| Function Name | CalcBmwHaptcFbPatNr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwHaptcFbPatNr_Cnt_T_enum | enum | 0 | 15 |

|  | BmwHaptcFbPatNrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwOscnActv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | BmwHaptcFbPatNr_Cnt_T_enum | enum | 0 | 15 |

|  | BmwHaptcFbPatNrLgc_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "CalcBmwHaptcFbPatNr" and "BmwHaptcFbPatNrLgc" Simulink block

#### Processing

Refer FDD

#### Local Function CalcBmwHaptcFbIntenNr



| Function Name | CalcBmwHaptcFbIntenNr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwHaptcFbIntenNr_Cnt_T_enum | enum | 0 | 15 |

|  | BmwHaptcFbIntenNrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwOscnActv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | BmwHaptcFbIntenNr_Cnt_T_enum | enum | 0 | 15 |

|  | BmwHaptcFbIntenNrLgc_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "CalcBmwHaptcFbIntenNr" and "BmwHaptcFbIntenNrLgc" Simulink block

#### Processing

Refer FDD

#### Local Function CalcHwOscnEna



| Function Name | CalcHwOscnEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PatChgReq_Cnt_T_logl | float32 | FALSE | TRUE |

|  | ActvTi_MilliSec_T_f32 | float32 | 0 | 60 |

|  | PasTi_MilliSec_T_f32 | float32 | 0 | 3 |

| Return Value | HwOscnEna_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of "CalcHwOscnEna" Simulink block

#### Processing

Refer FDD

#### Local Function CalcAmpAndFrq



| Function Name | CalcAmpAndFrq | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | HwOscnMotAmp_MotNwtMtr_T_f32 | float32 | 0 | 10 |

|  | HwOscnFrq_Hz_T_f32 | float32 | 10 | 50 |



#### Design Rationale

Implementation of "CalcAmpAndFrq" Simulink block

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

| 5 | CF020A_BmwHaptcFb_Design | See Synergy Sub Project Version |
