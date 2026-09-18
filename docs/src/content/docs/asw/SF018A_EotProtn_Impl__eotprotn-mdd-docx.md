---
title: 'SF018A_EotProtn_Impl — EotProtn_MDD'
description: 'Converted Word (.docx) document EotProtn_MDD.docx from module SF018A_EotProtn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `EotProtn_MDD.docx` (Word (.docx), 139 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Sarika Natu', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

EotProtn

Aug 16, 2017

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Change History



| SNo. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sarika Natu(KPIT Technologies) | 1.0 | 01-Oct-2015 |

| 2 | Implemented SF018A design version 1.5.0 | SB | 2.0 | 01-Jul-2016 |

| 3 | Updated Graph, Function Inputs, and Unit Test Considerations | Matthew Leser | 3.0 | 16-Aug-2017 |



Table of Contents

1EotProtn & High-Level Description5

2Design details of software module6

2.1Graphical representation of EotProtn6

2.2Data Flow Diagram7

2.2.1Component level DFD7

2.2.2Function level DFD7

3Constant Data Dictionary8

3.1Program (fixed) Constants8

3.1.1Embedded Constants8

4Software Component Implementation9

4.1Sub-Module Functions9

4.1.1Init: EotProtn_Init19

4.1.1.1Design Rationale9

4.1.1.2Module Outputs9

4.1.2Per: EotProtn_Per19

4.1.2.1Design Rationale9

4.1.2.2Store Module Inputs to Local copies9

4.1.2.3(Processing of function)………9

4.1.2.4Store Local copy of outputs into Module Outputs9

4.2Server Runables9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.4.1Local Function #19

4.4.1.1Design Rationale10

4.4.1.2Processing10

4.4.2Local Function #210

4.4.2.1Design Rationale10

4.4.2.2Processing10

4.4.3Local Function #310

4.4.3.1Design Rationale10

4.4.3.2Processing10

4.4.4Local Function #411

4.4.4.1Design Rationale11

4.4.4.2Processing11

4.4.5Local Function #511

4.4.5.1Design Rationale11

4.4.5.2Processing11

4.4.6Local Function #611

4.4.6.1Design Rationale11

4.4.6.2Processing11

4.4.7Local Function #711

4.4.7.1Design Rationale12

4.4.7.2Processing12

4.4.8Local Function #812

4.4.8.1Design Rationale12

4.4.8.2Processing12

4.4.9Local Function #912

4.4.9.1Design Rationale13

4.4.9.2Processing13

4.5GLOBAL Function/Macro Definitions13

5Known Limitations with Design14

6UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## EotProtn & High-Level Description

The End of Travel Protection function specifies performance attributes as the steering system approaches the mechanical end of travel of the steering gear.

## Design details of software module

### Graphical representation of EotProtn

### Data Flow Diagram

See FDD

#### Component level DFD

See FDD

#### Function level DFD

See FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant | Value |

| --- | --- |

| DAMPGPTSIZE_CNT_U08 | 2 |

| DAMPGVEHSPDSIZE_CNT_U08 | 4 |

| GAINVEHSPDSIZE_CNT_U08 | 5 |



## Software Component Implementation

### Sub-Module Functions

### Init: EotProtn_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: EotProtn_Per1

### Design Rationale

EotProtn_Per1 function is divided into various functions to reduce the cyclomatic complexity.

The limiting of ‘EotAssiSca’ output is performed in SoftEndStop subsystem in FDD. But in code it is limiting calculations are done where the output is calculated i.e. FildEotGain function.

The model is incorrectly handling a Case Statement by not having a default case. A solution was discussed with designers and has been implemented where the default case is Case 2 and Case 3.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | EotVelImpct | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | EotMotTqLim_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |



### Design Rationale

None

Note: Outputs of “EotVelImpct” function is - EotMotTqLim_MotNwtMtr_T_f32.

### Processing

Refer to the “EotVelImpct” subsystem of the Simulink model of the design

### Local Function #2



| Function Name | LimPosnDetd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RackTrvlLimrRngEna_Cnt_T_logl | boolean | False | True |

|  | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

| Return Value | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |



### Design Rationale

None

Note: Outputs of “LimPosnDetd” function is - LimPosn_HwDeg_T_f32.

### Processing

Refer to the “LimPosnDetd” subsystem of the Simulink model of the design

### Local Function #3



| Function Name | CalcEntrGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | EntrGain_Uls_T_f32 | float32 | 0 | 1 |



### Design Rationale

None

Note: Outputs of “CalcEntrGain” function is - EntrGain_Uls_T_f32.

### Processing

Refer to the “CalcEntrGain” subsystem of the Simulink model of the design

### Local Function #4



| Function Name | CalcExitGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | ExitGain_Uls_T_f32 | float32 | 0 | 1 |



### Design Rationale

Calculation of Filtered Handwheel torque is done after ‘CalcExitGain’ function is executed.

Note: Outputs of “CalcExitGain” function is - FildHwTq_HwNwtMtr_T_f32

### Processing

Refer to the “CalcExitGain” subsystem of the Simulink model of the design

### Local Function #5



| Function Name | CalcEotGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EntrGain_Uls_T_f32 | float32 | 0 | 1 |

|  | ExitGain_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | EotGain_Uls_T_f32 | float32 | 0 | 1 |



### Design Rationale

None

Note: Outputs of “CalcEotGain” function is - EotGain_Uls_T_f32

### Processing

Refer to the “CalcEotGain” subsystem of the Simulink model of the design

### Local Function #6



| Function Name | FildEotGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EotGain_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | EotAssiSca_Uls_T_f32 | float32 | 0 | 1 |



### Design Rationale

Limit of EotAssiSca is moved to local function FildEotGain.

Note: Outputs of “FildEotGain” function is - EotAssiSca_Uls_T_f32

### Processing

Refer to the “FildEotGain” subsystem of the Simulink model of the design

### Local Function #7



| Function Name | CalcEotDampg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | EotDampgCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |



### Design Rationale

None

Note: Outputs of “CalcEotDampg” function is - EotDampgCmd_MotNwtMtr_T_f32

### Processing

Refer to the “CalcEotDampg” calculation of the Simulink model of the design

### Local Function #8



| Function Name | EotActvCmdCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RackTrvlLimrDi_Cnt_T_logl | boolean | False | True |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -135

*Body truncated: document is longer than the excerpt shown here.*
