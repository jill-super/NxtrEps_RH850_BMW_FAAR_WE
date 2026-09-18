---
title: 'SF007A_SysFricLrng_Impl — SysFricLrng_MDD'
description: 'Converted Word (.docx) document SysFricLrng_MDD.docx from module SF007A_SysFricLrng_Impl.'
sidebar:
  hidden: true
---

> **Source:** `SysFricLrng_MDD.docx` (Word (.docx), 164 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

SysFricLrng

Oct 04, 2017

Prepared By:

Matthew Leser

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Basavaraja Ganeshappa | 1.0 | 24th Mar 2016 |

| Re base lined by pulling 1.3.1 | Basavaraja Ganeshappa | 2.0 | 25th Jul 2016 |

| Implementation of SF007A v2.0.0 & v2.1.0 | Krishna Anne | 3.0 | 3rd Oct 2016 |

| Updated to design version 2.2.0 | TATA | 4.0 | 05-Dec-16 |

| Updated to design version 2.4.0 | KK | 5.0 | 28-Feb-17 |

| Updated Diagram and added Unit Test Consideration | ML | 6.0 | 04-Oct-17 |



Table of Contents

1Introduction6

1.1Purpose6

2SysFricLrng High-Level Description7

3Design details of software module8

3.1Graphical representation of SysFricLrng8

3.2Data Flow Diagram9

3.2.1Component level DFD9

3.2.2Function level DFD9

4Constant Data Dictionary10

4.1Program (fixed) Constants10

4.1.1Embedded Constants10

5Software Component Implementation11

5.1Sub-Module Functions11

5.1.1Init: SysFricLrngInit111

5.1.1.1Design Rationale11

5.1.1.2Module Outputs11

5.1.2Per: SysFricLrngPer111

5.1.2.1Design Rationale11

5.1.2.2Store Module Inputs to Local copies11

5.1.2.3(Processing of function)………11

5.1.2.4Store Local copy of outputs into Module Outputs11

5.2Server Runnables11

5.2.1Server Runnable Name11

5.2.1.1Design Rationale11

5.2.1.2(Processing of function)………11

5.3Server Runnables12

5.3.1Server Runnable Name12

5.3.1.1Design Rationale12

5.3.1.2(Processing of function)………12

5.3.2Server Runnable Name12

5.3.2.1Design Rationale12

5.3.2.2(Processing of function)………12

5.3.3Server Runnable Name12

5.3.3.1Design Rationale12

5.3.3.2(Processing of function)………12

5.3.4Server Runnable Name12

5.3.4.1Design Rationale12

5.3.4.2(Processing of function)………12

5.3.5Server Runnable Name13

5.3.5.1Design Rationale13

5.3.5.2(Processing of function)………13

5.3.6Server Runnable Name13

5.3.6.2(Processing of function)………13

5.3.7Server Runnable Name13

5.3.7.2(Processing of function)………13

5.4Interrupt Functions13

5.4.1Interrupt Function Name13

5.4.1.1Design Rationale13

5.4.1.2(Processing of the ISR function)…..13

5.5Module Internal (Local) Functions14

5.5.1Local Function #114

5.5.1.1Design Rationale14

5.5.1.2Processing14

5.5.2Local Function #214

5.5.2.1Design Rationale14

5.5.2.2Processing14

5.5.3Local Function #315

5.5.3.1Design Rationale15

5.5.3.2Processing15

5.5.4Local Function #415

5.5.4.1Design Rationale15

5.5.4.2Processing15

5.5.5Local Function #516

5.5.5.1Design Rationale16

5.5.5.2Processing16

5.5.6Local Function #616

5.5.6.1Design Rationale16

5.5.6.2Processing16

5.5.7Local Function #716

5.5.7.1Design Rationale17

5.5.7.2Processing17

5.5.8Local Function #817

5.5.8.1Design Rationale17

5.5.8.2Processing17

5.5.8.317

5.5.9Local Function #917

5.5.9.1Design Rationale18

5.5.9.2Processing18

5.5.10Local Function #1018

5.5.10.1Design Rationale18

5.5.10.2Processing18

5.5.11Local Function #1118

5.5.11.1Design Rationale18

5.5.11.2Processing19

5.5.12Local Function #1219

5.5.12.1Design Rationale19

5.5.12.2Processing19

5.6GLOBAL Function/Macro Definitions19

6Known Limitations with Design20

7UNIT TEST CONSIDERATION21

Appendix AAbbreviations and Acronyms22

Appendix BGlossary23

Appendix CReferences24

## Introduction

### Purpose

MDD for System Friction Learning

## SysFricLrng High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of SysFricLrng

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

| INDEX0_CNT_U08 | 1 | CNT | 0U |

| INDEX1_CNT_U08 | 1 | CNT | 1U |

| INDEX2_CNT_U08 | 1 | CNT | 2U |

| INDEX3_CNT_U08 | 1 | CNT | 3U |

| SYSSATNFRICESTIMDMIN_HWNWMTR_F32 | 1 | HwNwMtr | 0.0F |

| SYSSATNFRICESTIMDMAX_HWNWMTR_F32 2 | 1 | HwNwMtr | 20.0F |

| SYSFRICESTIMDMIN_HWNWMTR_F32 | 1 | HwNwMtr | 0.0F |

| SYSFRICESTIMDMAX_HWNWMTR_F32 | 1 | HwNwMtr | 20.0F |

| SYSFRICOFFSMIN_HWNWMTR_F32 | 1 | HwNwMtr | -5.0F |

| SYSFRICOFFSMAX_HWNWMTR_F32 | 1 | HwNwMtr | 5.0F |



For rest of the constants, please refer Data Dictionary

## Software Component Implementation

The detailed design of the function is provided in the FDD.

### Sub-Module Functions

### Init: SysFricLrngInit1

### Design Rationale

In MDD, filters are initialized inside the for loop using switch case but in code filters are initialized one by one without any conditions.

In model, filters are initialized twice as it is not possible to use a variable for the filter initialization in the model. This is redundancy is not present in the code as variables are used for initializing the filters.

### Module Outputs

Refer FDD

### Per: SysFricLrngPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

### Server Runnable Name

ClrFricLrngOperMod

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnables

### Server Runnable Name

GetFricLrngData

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnable Name

GetFricOffsOutpDi

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnable Name

InitFricLrngTbl

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnable Name

SetFricLrngDatal

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnable Name

SetFricOffsOutpDi

### Design Rationale

Refer FDD

### (Processing of function)………

On server invocation call

### Server Runnable Name

#### GetFricData

#### Design Rationale

Refer FDD

To avoid calculating array indexing for updating PIMs Rte_Pim_FricLrngData()->Hys and Rte_Pim_FricLrngData()->RngCntr, performed casting the array argument back to it's actual type (similar to what we do with cal arrays) so we can use normal indexing.

### (Processing of function)………

On server invocation call

### Server Runnable Name

#### SetFricData

#### Design Rationale

Refer FDD

To avoid calculating array indexing for updating from PIMs Rte_Pim_FricLrngData()->Hys and Rte_Pim_FricLrngData()->RngCntr, performed casting the array argument back to it's actual type (similar to what we do with cal arrays) so we can use normal indexing.

### (Processing of function)………

On server invocation call

### Server Runnable Name

FricLrngShtDwn

### Design Rationale

Refer FDD

### (Processing of function)………

### Interrupt Functions

None

### Interrupt Function Name

None

### Design Rationale

NA

### (Processing of the ISR function)…..

NA

### Module Internal (Local) Functions

### Local Function #1



| Function Name | FricLearning | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SelHwAg_HwDeg_T_f32 | Float32 | -1440.0 | 1440.0 |

|  | SelColTq_HwNwtMtr_T_f32 | Float32 | -10 | 10 |

|  | VehSpdIdx_Cnt_T_u16 | Uint16 | 0 | 3 |

|  | HwVelDir_Cnt_T_u08 | Uint8 | 0 | 1 |

|  | LrngEna_Cnt_T_Logl | Boolean | FALSE | TRUE |

| Return Value | NA | NA | NA | NA |



### Design Rationale

### Processing

Refer to ‘FricLearning’ subsystem in FDD.

Following per instance data is updated.



| *Rte_Pim_RawAvrg() (Min:0, Max:20) |

| --- |

| Rte_Pim_SatnAvrgFric()[VehSpdIdx_Cnt_T_u16] (Min:0, Max:20) |



Also writes the outputs SysFricEstimd and SysSatnFricEstimd

### Local Function #2



| Function Name | RunningAndCalibrationModes | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | *FricOffs_HwNwtMtr_T_f32 | Float32 | -5.0 | +5.0 |

|  | 

*Body truncated: document is longer than the excerpt shown here.*
