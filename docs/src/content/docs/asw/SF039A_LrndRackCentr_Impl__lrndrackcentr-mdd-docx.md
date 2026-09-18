---
title: 'SF039A_LrndRackCentr_Impl — LrndRackCentr_MDD'
description: 'Converted Word (.docx) document LrndRackCentr_MDD.docx from module SF039A_LrndRackCentr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `LrndRackCentr_MDD.docx` (Word (.docx), 108 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

LrndRackCentr

October 26, 2017

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | ML | 1.0 | 26-Oct-2017 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2LrndRackCenter & High-Level Description6

3Design details of software module7

3.1Graphical representation of LrndRackCentr7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: LrndRackCentrInit19

5.1.1.1Design Rationale9

5.1.2Per: LrndRackCentrPer19

5.1.2.1Design Rationale9

5.2Server Runnable9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Description9

5.4.2Local Function #29

5.4.2.1Description10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## LrndRackCenter & High-Level Description

Refer FDD.

## Design details of software module

### Graphical representation of LrndRackCentr

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

### Init: LrndRackCentrInit1

Refer FDD Simulink model

### Design Rationale

None

### Per: LrndRackCentrPer1

Refer FDD Simulink Model

### Design Rationale

Refer to Anomaly EA4#17201. Implementation deviates from design to fix for build.

### Server Runnable

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | ManLrnRackCentr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | MotTqCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | None |  |  |  |



### Description

Implementation of ‘MANUAL LEARN RACK CENTER’ subsystem.

### Local Function #2



| Function Name | ChkRackCentr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTrvl_HwDeg_T_f32 | float32 | 0 | 2880 |

|  | RackCentr_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | *RackCentrMotAgVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | *RackCentrCmpl_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |



### Description

Implementation of ‘Confirm Rack Center Found’ subsystem.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

Refer to Anomaly EA4#17201. Implementation deviates from design to fix for build.

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

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD – SF039A_LrndRackCentr_Design | See Synergy Subproject verison |
