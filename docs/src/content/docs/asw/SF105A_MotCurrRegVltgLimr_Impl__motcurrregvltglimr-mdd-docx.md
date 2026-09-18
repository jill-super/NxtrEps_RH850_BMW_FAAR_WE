---
title: 'SF105A_MotCurrRegVltgLimr_Impl — MotCurrRegVltgLimr_MDD'
description: 'Converted Word (.docx) document MotCurrRegVltgLimr_MDD.docx from module SF105A_MotCurrRegVltgLimr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotCurrRegVltgLimr_MDD.docx` (Word (.docx), 121 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Module Design Document

For

‘MotCurrRegVltgLimr’

VERSION: 5.0

DATE: 08-Nov-2017

Prepared By:

TATA ELXSI,

TRIVANDRUM, INDIA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Selva Sengottaiyan | 1.0 | 26-May-2015 |

| 2 | Updated graphical representation and added local function information | Nick Saxton | 2.0 | 13-Apr-2016 |

| 3 | Updated for FDD v2.1.0 | Matthew Leser | 3.0 | 7-Nov-2016 |

| 4 | Updated to fix Anomaly EA4#9045 | Matthew Leser | 4.0 | 04-Jan-2017 |

| 5 | Updated for FDD v3.0.0 | TATA | 5.0 | 08-Nov-2017 |



Table of Contents

1Abbrevations And Acronyms5

2References6

3High-Level Description7

4Design details of software module8

4.1Graphical representation8

4.2Data Flow Diagram8

4.2.1Module level DFD8

4.2.2Sub-Module level DFD8

4.3COMPONENT FLOW DIAGRAM8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Constant Data Dictionary10

6.1Program(fixed) Constants10

6.1.1Embedded Constants10

6.1.1.1Local10

6.1.1.2Global10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation11

7.1Sub-Module Functions11

7.1.1Initialization Functions11

7.1.1.1INIT: MotCurrRegVltgLimrInit111

7.1.1.1.1Design Rationale11

7.1.1.1.2Module Outputs11

7.1.1.1.3Module Internal11

7.1.2PERIODIC FUNCTIONS11

7.1.2.1INIT: MotCurrRegVltgLimrPER111

7.1.2.1.1Design Rationale11

7.1.2.1.2Module Outputs11

7.1.3Interrupt Functions11

7.1.4Server runnables12

7.1.4.1.1Store Local copy of outputs into Module Outputs12

7.1.5Local Function/Macro Definitions12

7.1.5.1.1Local function #112

7.1.5.1.2Local function #212

7.1.5.1.3Local function #312

7.1.5.1.4Local function #413

7.1.5.1.5Local function #513

7.1.6GLObAL Function/Macro Definitions13

7.1.7Tranisition FUNCTIONS13

8Known Limitations With Design14

9UNIT TEST CONSIDERATION15

10Appendix16

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | MDD Guidelines | Process 4.02.01 |

| 2 | Software Naming Conventions | Process 4.02.01 |

| 3 | Software Design and Coding standards | 2.1 |

| 4 | FDD – SF105A_MotCurrRegVltgLimr_Design | See Synergy sub project version |



## High-Level Description

None

## Design details of software module

### Graphical representation

### Data Flow Diagram

Refer FDD

### Module level DFD

Refer FDD

### Sub-Module level DFD

Refer FDD

### COMPONENT FLOW DIAGRAM

Refer FDD

## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None |  |  |  |  |



### Variable definition for enumerated types



| Enum Name | Element Name | Value |

| --- | --- | --- |

| None |  |  |



## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MODIDXHILIM_VOLT_F32 | Single precision float | Volt | 1 |

| MODIDXLOLIM_VOLT_F32 | Single precision float | Volt | 0 |

| BITMASK1_CNT_U08 | Uint8 | CNT | 1U |

| BITMASK2_CNT_U08 | Uint8 | CNT | 2U |

| BITMASK4_CNT_U08 | Uint8 | CNT | 4U |



### Global



| Constant Name |

| --- |



### Module specific Lookup Tables Constants

None

## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

MotCurrRegVltgLimrInit1

### INIT: MotCurrRegVltgLimrInit1

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Refer ‘MotCurrRegVltgLimrInit’ block in FDD

### Module Internal

None

### PERIODIC FUNCTIONS

### INIT: MotCurrRegVltgLimrPER1

### Design Rationale

As per FDD, dMotCurrRegVltgLimrMotVltgDecouplFbDax, dMotCurrRegVltgLimrMotVltgDecouplFbQax renamed with dMotCurrRegVltgLimrMotVltgDecoupldFbDax, dMotCurrRegVltgLimrMotVltgDecouplFbQax in the source file. And also dMotCurrRegVltgLimrMotCurrCmdErr(display variable) is nowhere used in source file. That variable davinci definition is removed.

### Module Outputs

Design follows implemenetation in FDD.

### Interrupt Functions

None

### Server runnables

None

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

### Local function #1



| Function Name | KpKiCtrl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotPropGain_Ohm_T_f32 | Float32 | 0 | 2.25 |

|  | MotIntglGain_Ohm_T_f32 | Float32 | 0 | 3.6 |

|  | SysSt_Cnt_T_enum | Enum | SYSST_DI | SYSST_WRMININ |

|  | CmdErr_Ampr_T_f32 | Float32 | -200 | 400 |

|  | *MotVltgIntglCmdPrev_Volt_T_f32 | Float32 | -1000 | 1000 |

|  | *MotCurrRegVltgLimrMotVltgPropCmd_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | *MotCurrRegVltgLimrMotVltgIntglPreLim_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | MotVltgIntglLoLim_Volt_T_f32 | Float32 | -31 | 0 |

|  | MotVltgIntglHiLim_Volt_T_f32 | Float32 | 0 | 31 |

|  | *MotVltgPropCmd_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | *MotVltgIntglCmd_Volt_T_f32 | Float32 | 6 | 26.5 |



- * MotVltgPropCmd_Volt_T_f32 and * MotVltgIntglCmd_Volt_T_f32 are outputs of this function.

### Local function #2



| Function Name | ErrorCalcQax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | QaxCurrCmd_Ampr_T_f32 | Float32 | -200 | 200 |

|  | QaxRplCmd_Ampr_T_f32 | Float32 | -29 | 29 |

|  | QaxCoggCmd_Ampr_T_f32 | Float32 | -6 | 6 |

|  | QaxCurrModif_Ampr_T_f32 | Float32 | -200 | 200 |

|  | * QaxCmdFinal_Ampr_T_f32 | Float32 | -200 | 200 |

| Returns | CmdErrQax_Ampr_T_f32 | Float32 | -200 | 400 |



- *QaxCmdFinal_Ampr_T_f32 is also an output of this function.

### Local function #3



| Function Name | LoaScaFac | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CurrLoaMtgtnEn_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | IvtrLoaMtgtnEn_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | MotCtrlDualEcuMotCtrlMtgtnEna_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | FetLoaMtgtnEna_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | *CurrLoaScaFac_Uls_T_f32 | Float32 | 0 | 1 |

|  | *IvtrLoaScaFac_Uls_T_f32 | Float32 | 0 | 1 |

|  | *DualEcuScaFac_Uls_T_f32 | Float32 | 0 | 1 |

|  | *FetScaFac_Uls_T_f32 | Float32 | 0.0F | 1.0F |



- *CurrLoaScaFac_Uls_T_f32, *IvtrLoaScaFac_Uls_T_f32, and *DualEcuScaFac_Uls_T_f32  are outputs of this function.

### Local function #4



| Function Name | MotCurr_Pred | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotInduQaxEstimdIvs_IvsHenry_T_f32 | Float32 | 2240 | 33334 |

|  | MotREstimd_Ohm_T_f32 | Float32 | 0.005 | 0.12565 |

|  | CurrQax_Ampr_T_f32 | Float32 | -200 | 200 |

|  | MotVltgQaxPrev_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | CurrDax_Ampr_T_f32 | Float32 | -200 | 200 |

|  | MotVltgDaxPrev_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | MotBackEmfVltg_Volt_T_f32 | Float32 | -101.25 | 101.25 |

|  | ReacncQax_Ohm_T_f32 | Float32 | -0.5 | 0.5 |

|  | ReacncDax_Ohm_T_f32 | Float32 | -0.5 | 0.5 |

|  | MotInduDaxEstimdIvs_IvsHenry_T_f32 | Float32 | 2240 | 33334 |

|  | MotCurrRegVltgLimrMotCurrPredEna_Cnt_T_f32 | Boolean | FALSE | TRUE |

|  | MotCtrlCurrPredTi_NanoSec_T_f32 | Float32 | 0 | 125000 |

|  | *MotCurrQaxPred_Ampr_T_f32 | Float32 | -200 | 200 |

|  | *MotCurrDaxPred_Ampr_T_f32 | Float32 | -200 | 200 |



- *MotCurrQaxPred_Ampr_T_f32 and *MotCurrDaxPred_Ampr_T_f32 are outputs of this function.

### Local function #5



| Function Name | Decoder |

*Body truncated: document is longer than the excerpt shown here.*
