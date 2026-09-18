---
title: 'ES210A_EcuTMeas_Impl — EcuTMeas_MDD'
description: 'Converted Word (.docx) document EcuTMeas_MDD.docx from module ES210A_EcuTMeas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `EcuTMeas_MDD.docx` (Word (.docx), 111 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Shruthi Raghavan', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

EcuTMeas

26-Sep-2017

Prepared By:

Brendon Binder,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Sl.No | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1.0 | 23-Mar-2015 |

| 2 | ADC Hooks are added as input | KK | 2.0 | 21-Mar-2016 |

| 3 | Added local constants for paramterbyte definitions | AJM | 3.0 | 10-Apr-2017 |

| 4 | Updated the graphical representation (all cal ports are removed), added local constants, design rationale, known limitations and unit tests considerations. Updated to the new template | Shruthi Raghavan | 4.0 | 08-Aug-2017 |

| 5 | Updated the DaVinci model (added new output). | Brendon Binder | 5.0 | 26-Sep-2017 |



Table of Contents

1Introduction4

1.1Purpose4

2EcuTMeas & High-Level Description5

3Design details of software module6

3.1Graphical representation of EcuTMeas6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: EcuTMeasInit18

5.1.1.1Design Rationale8

5.1.2Per: EcuTMeasPer18

5.1.2.1Design Rationale8

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.4.1Local Function #18

5.4.1.1Design Rationale8

5.5GLOBAL Function/Macro Definitions8

5.5.1GLOBAL Function #18

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

Module design document for EcuTMeas

## EcuTMeas & High-Level Description

Measures and diagnoses an analog based temperature sensor on ECU.

This particular design can tolerate a transfer function that is not necessarily linear but can be interpolated with 8 different XY pairs.

## Design details of software module

### Graphical representation of EcuTMeas

### Data Flow Diagram

#### Component level DFD

Refer FDD simulink model

#### Function level DFD

Refer FDD simulink model

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value | Defined In |

| --- | --- | --- | --- | --- |

| ECUTFILDMIN_DEGCGRD_F32 | Single Precision Float | DegCgrd | -50.0F | EcuTMeas.c |

| ECUTFILDMAX_DEGCGRD_F32 | Single Precision Float | DegCgrd | 150.0F | EcuTMeas.c |

| NROFSNSRXYPT_CNT_U08 | 1 | Cnt | 8U* | EcuTMeas_Cfg_private.h |

| Refer DataDict.m file for other constants | - | - | - |  |



*This the value might change based on EcuTx and EcuTy table size.

## Software Component Implementation

### Sub-Module Functions

### Init: EcuTMeasInit1

Refer FDD simulink model

### Design Rationale

‘Filter Initialization’ block in the FDD uses ‘FilLpInit’ library block twice rather than just once due to a design limitation with the Library block (see ‘Known limitations with design’). However, code has no such limitation. In code, the value to be written to the state variable according to the logic in ‘State Variable Initialization’ is calculated first. Then, the ‘FilLpInit’ library function is called just once and that will initialize the state variable with this calculated value and the gain according to the set frequency & time.

### Per: EcuTMeasPer1

Refer FDD Simulink Model

### Design Rationale

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | - | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A | - | - | - |

| Return Value | N/A | - | - | - |



### Design Rationale

N/A

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name | - | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A | - | - | - |

| Return Value | N/A | - | - | - |



## Known Limitations with Design

- The FilLpInit block in the model cannot accept a variable as input for initialization of the state variable.

## UNIT TEST CONSIDERATION

- This component uses config params for some configurable constants. However for testing these in PIL/SIL, please use the following strategy:

- Rename the EcuTMeas_Cfg_private_pil.h file in tools/local/include folder to EcuTMeas_Cfg_private.h

- Replace the EcuTMeas_Cfg_private.h file in tools/local/generate folder with the above file.

Now, Tessy must be able to modify the values of these config params. We should then test them with the range that is given in their definition in the DataDict.m file

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document. (See references) |



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

| 3 | EA4 Software Naming Conventions.doc | 01.01.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | ES210A_EcuTMeas_Design (FDD) | Refer subproject verison on Synergy |
