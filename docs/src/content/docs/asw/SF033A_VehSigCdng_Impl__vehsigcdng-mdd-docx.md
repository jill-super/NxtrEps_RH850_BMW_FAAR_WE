---
title: 'SF033A_VehSigCdng_Impl — VehSigCdng_MDD'
description: 'Converted Word (.docx) document VehSigCdng_MDD.docx from module SF033A_VehSigCdng_Impl.'
sidebar:
  hidden: true
---

> **Source:** `VehSigCdng_MDD.docx` (Word (.docx), 132 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Michael Story', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 10

## Converted content

For

VehSigCdng

Sep 20, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Spandana BalaniChange History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1 | 13-Jul-2015 |

| 2 | Updated for FDD v2.0.0 | NS | 2 | 2-Jun-2016 |

| 3 | Updated for FDD v2.2.0 | SB | 3 | 20-Sep-2016 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2VehSigCdng High-Level Description5

3Design details of software module6

3.1Graphical representation of VehSigCdng6

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1.1Sub-Module Functions10

5.1.2Interrupt Service Routines10

5.1.3Server Runnable Functions10

5.1.4Module Internal (Local) Functions10

5.1.5Transition Functions11

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

## VehSigCdng High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of VehSigCdng

### Data Flow Diagram

#### Component level DFD

Refer to FDD

#### Function level DFD

Refer to FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

See .m file

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module VehSigCdngInit1()

#### Periodic sub-module VehSigCdngPer1()

Design Rationale - Fault Injection client call is conditional compiled based on “FLTINJENA” build constant.

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Local Function #1

Refer to VehSpd block in the model



| Function Name | VehSigCdng_VehSpd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpdSerlCom_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehSpdOvrd_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdOvrdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehSpd_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | N/A |  |  |  |



Notes: VehSpd_Kph_T_f32,  VehSpdVld_Cnt_T_logl are the outputs of the function

#### Local Function #2

Refer to VehLgtA block in the model



| Function Name | VehSigCdng_VehLgtA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLgtASerlCom_MpSecSq_T_f32 | Float32 | -180 | 180 |

|  | VehLgtAVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehLgtA_KphpS_T_f32 | Float32 | -50 | 50 |

|  | VehLgtAVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |



Notes: VehLgtA_KphpS_T_f32, VehLgtAVld_Cnt_T_logl are the outputs of the function

#### Local Function #3

Refer to VehLatA block in the model



| Function Name | VehSigCdng_VehLatA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLatASerlCom_MpSecSq_T_f32 | Float32 | -10 | 10 |

|  | VehLatAVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehLatA_MpSecSq_T_f32 | Float32 | -10 | 10 |

|  | VehLatAVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |



Notes: VehLatA_MpSecSq_T_f32, VehLatAVld_Cnt_T_logl are the outputs of the function

#### Local Function #4

Refer to VehYawRate block in the model



| Function Name | VehSigCdng_VehYawRate | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehYawRateSerlCom_DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehYawRate_DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |



Notes: VehYawRate_DegpS_T_f32, VehYawRateVld_Cnt_T_logl are the outputs of the function

#### Local Function #5

Refer to “Lateral Acceleration Estimation” block in the model



| Function Name | VehSigCdng_LatAEstmn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehYawRate_DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVld_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehSpd_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehLatAEstimd_MtrPerSecSqd_T_f32 | Float32 | -10 | 10 |

|  | VehLatAEstimdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |



Notes: VehLatAEstimd_MtrPerSecSqd_T_f32, VehLatAEstimdVld_Cnt_T_logl  are the outputs of the function

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

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

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD – SF033A_VehSigCdng_Design | See Synergy Sub project version |
