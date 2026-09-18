---
title: 'ES340A_SerlComTrcvIf_Impl — SerlComTrcvIf_MDD'
description: 'Converted Word (.docx) document SerlComTrcvIf_MDD.docx from module ES340A_SerlComTrcvIf_Impl.'
sidebar:
  hidden: true
---

> **Source:** `SerlComTrcvIf_MDD.docx` (Word (.docx), 107 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Byrski, Krzysztof', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 9

## Converted content

For

SerlComTrcvIf

February 21, 2018

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

| Initial version (based on Design 1.1.0) | Krzysztof Byrski | 1 | 21-Feb-2018 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2SerlComTrcvIf & High-Level Description5

3Design details of software module6

3.1Graphical representation of SerlComTrcvIf6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: SerlComTrcvIfInit18

5.1.2Per: SerlComTrcvIfPer18

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions9

5.4.1Local Function MonitorERRN9

5.4.2Local Function ReadAndAnalyze9

5.4.3Local Function AnalyzeRegister9

5.4.4Local Function ParityErrorCheck10

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

Module Design Document for SerlComTrcvIf.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## SerlComTrcvIf & High-Level Description

The Serial Communication Transceiver Interface function monitors error status of FlexRay transceiver, reads the Status Registers via SPI and sets appropriate NTCs.

## Design details of software module

### Graphical representation of SerlComTrcvIf

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

| SERLCOMTRCVIFNTCMASKBIT5_CNT_U08 | 1 | Cnt | 32 |

| SERLCOMTRCVIFNTCMASKBIT7_CNT_U08 | 1 | Cnt | 128 |

| SERLCOMTRCVIFRESDBITS_CNT_U16 | 1 | Cnt | 20480 |

| SERLCOMTRCVIFSPIERRCNTRMAX_CNT_U08 | 1 | Cnt | 1 |

| STMONRERRPIN_CNT_U08 | 1 | Cnt | 1 |

| STREADANDDECOD_CNT_U08 | 1 | Cnt | 2 |

| SERLCOMTRCVIFMASKBITS11TO14_CNT_U16 | 1 | Cnt | 0x7800 |

| SERLCOMTRCVIFMASKBITS5TO10_CNT_U16 | 1 | Cnt | 0x7E0 |



## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: SerlComTrcvIfInit1

#### Design Rationale

Refer FDD

#### Module Outputs

None

#### Per: SerlComTrcvIfPer1

#### Design Rationale

Refer FDD

#### Store Module Inputs to Local copies

None

#### (Processing of function)………

Refer FDD

#### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### Local Function MonitorERRN



| Function Name | MonitorERRN | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | None |  |  |  |



#### Design Rationale

Implementation of Simulink block "MonitorERRN".

#### Processing

Refer Simulink block "MonitorERRN".

#### Local Function ReadAndAnalyze



| Function Name | ReadAndAnalyze | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | None |  |  |  |



#### Design Rationale

Implementation of Simulink block "ReadAndAnalyze".

#### Processing

Refer Simulink block "ReadAndAnalyze".

#### Local Function AnalyzeRegister



| Function Name | AnalyzeRegister | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RegIn_Cnt_T_u16 | uint16 | 0 | 65535 |

| Return Value | NtcStsInfo_Cnt_T_u08 | uint8 | 0 | 128 |



#### Design Rationale

Implementation of Simulink block "AnalyzeRegister".

#### Processing

Refer Simulink block "AnalyzeRegister".

#### Local Function ParityErrorCheck



| Function Name | ParityErrorCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RegIn_Cnt_T_u16 | uint16 | 0 | 65535 |

| Return Value | Parity_Cnt_T_logl | boolean | FALSE | TRUE |



#### Design Rationale

Implementation of Simulink block "ParityErrorCheck".

#### Processing

Refer Simulink block "ParityErrorCheck".

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

| 5 | ES340A_SerlComTrcvIf_Design | See Synergy Sub Project Version |
