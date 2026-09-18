---
title: 'CF080A_BmwVehSpd_Impl — BmwVehSpd_MDD'
description: 'Converted Word (.docx) document BmwVehSpd_MDD.docx from module CF080A_BmwVehSpd_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwVehSpd_MDD.docx` (Word (.docx), 149 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 12

## Converted content

For

BmwVehSpd

June 22, 2018

Prepared By:

Marek Brykczyński,

Nexteer Automotive,

Tychy, PolandChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial version | Matthew Leser | 1.0 | 27-Feb-2018 |

| Updated according to design 3.0.0 | Marek Brykczyński | 2.0 | 25-Jun-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2BmwVehSpd High-Level Description6

3Design details of software module7

3.1Graphical representation of BmwVehSpd7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1BmwVehSpdInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2BmwVehSpdPer19

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.2Server Runnables9

5.3Interrupt Functions9

5.3.1Interrupt Function Name9

5.4Module Internal (Local) Functions9

5.4.1Cntr9

5.4.2VehSpdVldCalcn10

5.4.3VehSpdRateLim10

5.4.4ProcessSecondAndGateState10

5.4.5ProcessThirdAndGateState10

5.4.6ProcessSixthAndGateState10

5.4.7ProcessFourthAndGateState11

5.4.8ProcessThridConditionOfOrGate11

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CPlease references16

## Introduction

### Purpose

Module Design Document for CF080A_BmwVehSpd_Impl

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## BmwVehSpd High-Level Description

The BmwVehSpd software component is responsible for determining the Vehicle Speed.

## Design details of software module

Please refer FDD

### Graphical representation of BmwVehSpd

### Data Flow Diagram

Please refer FDD

#### Component level DFD

Please refer FDD

#### Function level DFD

Please refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file for constants |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### BmwVehSpdInit1

### Design Rationale

Please refer FDD

### Module Outputs

None

### BmwVehSpdPer1

### Design Rationale

Please refer FDD.

### Module Outputs

None

### Server Runnables

None

### Interrupt Functions

None

### Interrupt Function Name

None

### Module Internal (Local) Functions

#### Cntr



| Function Name | Cntr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CntrTrigInp_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SigValVld_Cnt_T_logl | const pointer to boolean | FALSE | TRUE |

|  | CdnDurnSigValVld_Cnt_T_logl | const pointer to boolean | FALSE | TRUE |

| Return Value | None | - | - | - |



#### VehSpdVldCalcn



| Function Name | VehSpdVldCalcn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwSecurVehSpdSts_Cnt_T_enum | uint8 | 1 | 15 |

| Return Value | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |



#### VehSpdRateLim



| Function Name | VehSpdRateLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwSecurVehSpdSts_Cnt_T_enum | uint8 | 1 | 15 |

|  | IntEpsVehSpd_Kph_T_f32 | float32 | 0 | 350 |

| Return Value | *Rte_Pim_VehSpdLimPrev() | float32 | 0 | 511 |



#### ProcessSecondAndGateState



| Function Name | ProcessSecondAndGateState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwCogVehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwCogVehSpdQlfrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwCogVehSpdQlfr_Cnt_T_enum | uint8 | 1 | 15 |

| Return Value | SecondAndGateEval_Cnt_T_logl | boolean | FALSE | TRUE |



#### ProcessThirdAndGateState



| Function Name | ProcessThirdAndGateState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwCogVehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwCogVehSpdQlfrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwCogVehSpdQlfr_Cnt_T_enum | uint8 | 1 | 15 |

| Return Value | ThirdAndGateEval_Cnt_T_logl | boolean | FALSE | TRUE |



#### ProcessSixthAndGateState



| Function Name | ProcessSixthAndGateState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwPinionAgQlfr_Cnt_T_enum | boolean | FALSE | TRUE |

| Return Value | SixthAndGateEval_Cnt_T_logl | boolean | FALSE | TRUE |



#### ProcessFourthAndGateState



| Function Name | ProcessFourthAndGateState | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ThirdAndGateEval_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SixthAndGateEval_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | function’s return value | boolean | FALSE | TRUE |



#### ProcessThridConditionOfOrGate



| Function Name | ProcessThridConditionOfOrGate | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | BmwCogVehSpdQlfrVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | CdnDurnSigValVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | BmwCogVehSpdQlfr_Cnt_T_enum | uint8 | 1 | 15 |

| Return Value | LogicResult_Cnt_T_logl | boolean | FALSE | TRUE |



### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None.

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

- Automotive SPICE® Process Please reference Model (PRM)

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



#### Please references
