---
title: 'SF073A_ClsdLoopHys_Impl — ClsdLoopHys_MDD'
description: 'Converted Word (.docx) document ClsdLoopHys_MDD.docx from module SF073A_ClsdLoopHys_Impl.'
sidebar:
  hidden: true
---

> **Source:** `ClsdLoopHys_MDD.docx` (Word (.docx), 147 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 10

## Converted content

For

ClsdLoopHys

July 17, 2018

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

| Initial version | Marek Brykczyński | 1 | 10-May-2018 |

| Added: New input port and local function Modified: the function Interpolate | Marek Brykczyński | 2 | 17-July-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2ClsdLoopHys & High-Level Description5

3Design details of software module6

3.1Graphical representation of ClsdLoopHys6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: ClsdLoopHysInit18

5.1.2Per: ClsdLoopHysPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1Interpolate9

5.4.2IntgtrLimCalcn9

5.4.3CompCalcn19

5.4.4CompCalcn19

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

The Module Design Document for SF073A_ClsdLoopHys_Impl.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## ClsdLoopHys & High-Level Description

The Closed Loop Hysteresis function shall provide a controllable hysteresis shaped Reference Handwheel Torque component based on a current Rack Load.

## Design details of software module

### Graphical representation of ClsdLoopHys

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

#### Init: ClsdLoopHysInit1

#### Design Rationale

Refer FDD

#### Module Outputs

Refer FDD

#### Per: ClsdLoopHysPer1

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

#### Interpolate



| Function Name | Interpolate | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Y_Tbl_1D: - ClsdLoopHysDelta - ClsdLoopHysGain - ClsdLoopHysRho* | Pointer to const table with uint16 | 0 | 10240 / 20480* |

|  | VehSpd_Kph_T_u9p7 | uint16 | 0 | 65408 |

| Return Value | A result of a conversion of fixed-point to float32 | float32 | 0 | 10 / 20* |



#### IntgtrLimCalcn



| Function Name | IntgtrLimCalcn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwVel_HwRadPerSec_T_f32 | float32 | -42 | 42 |

|  | HwAg_HwRad_T_f32 | float32 | -25.13274192 | 25.13274192 |

|  | UpprIngtrLim_Uls_T_f32 | const pointer to float32 | -5 | 5 |

|  | LwrIngtrLim_Uls_T_f32 | const pointer to float32 | -5 | 5 |

| Return Value | - | - | - | - |



#### CompCalcn1



| Function Name | CompCalcn1 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwVel_HwRadPerSec_T_f32 | float32 | -42 | 42 |

|  | HysBasFac_Uls_T_f32 | float32 | -10 | 10 |

|  | Delta_Uls_T_f32 | float32 | 0 | 10 |

| Return Value | Result_T_Uls_f32 | Float32 | -42000 | 42000 |



#### CompCalcn1



| Function Name | CompCalcn2 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwVel_HwRadPerSec_T_f32 | float32 | -42 | 42 |

|  | HysBasFac_Uls_T_f32 | float32 | -10 | 10 |

|  | Delta_Uls_T_f32 | float32 | 0 | 10 |

| Return Value | Result_T_Uls_f32 | float32 | -4200 | 37800 |



#### SysFricOffsLimdCalc



| Function Name | SysFricOffsLimdCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_u9p7 | uint16 | 0 | 65408 |

|  | SysFricOffs_HwNwtMtr_T_f32 | float32 | -5 | 5 |

| Return Value | return value of conversion from u2p14 to float32 | float32 | 0 | 2 |



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

| 5 | SF073A_ClsdLoopHys_Design | See Synergy Sub Project Version |
