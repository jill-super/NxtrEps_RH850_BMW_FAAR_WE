---
title: 'SF006A_TEstimn_Impl — TEstimn_MDD'
description: 'Converted Word (.docx) document TEstimn_MDD.docx from module SF006A_TEstimn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `TEstimn_MDD.docx` (Word (.docx), 131 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 6

## Converted content

For

TEstimn

06-Apr-2018

Prepared By:

Shawn Penning,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 17-Sep-2015 |

| Updated to Design v2.2.0 | Matthew Leser | 2 | 26-Apr-2017 |

| Updated Graph and added new local function | Matthew Leser | 3 | 06-Dec-2017 |

| Added local constants and unit test considerations. | SPP | 4 | 06-Apr-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2TEstimn High-Level Description5

3Design details of software module6

3.1Graphical representation of TEstimn6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: TEstimnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: TEstimnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

### Scope

## TEstimn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of TEstimn

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

#### Local Constants

#define TESTIMNASSIMECHTHILIM_DEGCGRD_F32150.0F

#define TESTIMNASSIMECHTLOLIM_DEGCGRD_F32(-50.0F)

#define TESTIMNFETTHILIM_DEGCGRD_F32200.0F

#define TESTIMNFETTLOLIM_DEGCGRD_F32(-50.0F)

#define TESTIMNMAGTHILIM_DEGCGRD_F32150.0F

#define TESTIMNMAGTLOLIM_DEGCGRD_F32(-50.0F)

#define TESTIMNWIDGTHILIM_DEGCGRD_F32300.0F

#define TESTIMNWIDGTLOLIM_DEGCGRD_F32(-50.0F)

#define DUALECUSTSIDX_CNT_U08               ((uint8)0U)

#define SNGECUSTSIDX_CNT_U08                ((uint8)1U)

#define EXPCOEFF_ULS_F32                    (-1.0F)

#define SILLFILVALMIN_ULS_F32               (-2431500.0F)

#define SILLFILVALMAX_ULS_F32               (1001200.0F)

#define SILPFILVALMIN_ULS_F32               (0.0F)

#define SILPFILVALMAX_ULS_F32               (62500.0F)

#define ASSIMECHLLFILVALMIN_ULS_F32         (-4577000.0F)

#define ASSIMECHLLFILVALMAX_ULS_F32         (1716400.0F)

#define ASSIMECHLPFILVALMIN_ULS_F32         (0.0F)

#define ASSIMECHLPFILVALMAX_ULS_F32         (1764.0F)

#define CULLFILVALMIN_ULS_F32               (-2431500.0F)

#define CULLFILVALMAX_ULS_F32               (1001200.0F)

#define CULPFILVALMIN_ULS_F32               (0.0F)

#define CULPFILVALMAX_ULS_F32               (62500.0F)

#define MAGLLFILVALMIN_ULS_F32              (-2431500.0F)

#define MAGLLFILVALMAX_ULS_F32              (1001200.0F)

#define MAGLPFILVALMIN_ULS_F32              (0.0F)

#define MAGLPFILVALMAX_ULS_F32              (62500.0F)

#define FILVALMIN_ULS_F32                   (0.0F)

#define TESTIMNFETMTGTNIDX_CNT_U08          ((uint8)2U)

#define TESTIMNIGNTIOFFTHD_CNT_F32          (10000.0F)

#define FETLOABITMASK_CNT_U08               ((uint8)4U)

## Software Component Implementation

### Sub-Module Functions

### Init: TEstimnInit1

### Design Rationale

Refer FDD for the functionality.

### Module Outputs

Refer FDD

### Per: TEstimnPer1

### Design Rationale

In ‘AssistMechanismLeadLagFilterRe-Initialization’ block, blocks ‘AssistMechanismInitEnable’ and ‘AssistMechanismInitDisable’ have similar logic except for some calculations related to inputs.  So the differences are implemented in ‘if-else’ statement and common logic is implemented after ‘if-else’ statements in the SW.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | FltMtgtnCalSeln | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FetLoaMtgtnEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | DualEcuFltMtgtnEna_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | NA | NA | NA | NA |



### Design Rationale

Implementation of ‘Fault Mitigation Calibration Selection’ block in FDD (To reduce cyclomatic complexity & path count in Per1).

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

- None

## UNIT TEST CONSIDERATION

Calculate TEstimnSiLLFilCoeffB0 as per following equation:

TEstimnSiLLFilCoeffB0= -1*[(TEstimnSiLLFilCoeffA1-1)+TEstimnSiLLFilCoeffB1]

Calculate TEstimnCuLLFilCoeffB0 as per following equation:

TEstimnCuLLFilCoeffB0= -1*[(TEstimnCuLLFilCoeffA1-1)+TEstimnCuLLFilCoeffB1]

Calculate TEstimnMagLLFilCoeffB0 as per following equation:

TEstimnMagLLFilCoeffB0= -1*[(TEstimnMagLLFilCoeffA1-1)+TEstimnMagLLFilCoeffB1]

Calculate TEstimnAssiMechLLFilCoeffB0 as per following equation:

TEstimnAssiMechLLFilCoeffB0= -1*[(TEstimnAssiMechLLFilCoeffA1-1)+TEstimnAssiMechLLFilCoeffB1]

Anomaly 20644 Issue 1B and 1C were not addressed due to time considerations. Anomaly 19666 issue 4 is a test issue that should be addressed by test team but does not affect design or code.

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

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | EA4 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD : SF006A_ TEstimn_Design | See Synergy sub project version |
