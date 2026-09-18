---
title: 'CM640B_MotAg1Meas_Impl — MotAg1Meas_MDD'
description: 'Converted Word (.docx) document MotAg1Meas_MDD.docx from module CM640B_MotAg1Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAg1Meas_MDD.docx` (Word (.docx), 180 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 3

## Converted content

Module Design Document

For

Motor Angle 1 Measurement

May 04, 2018

Prepared By:

Avinash James

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Avinash James | 1.0 | 07-Jun-2016 |

| Removed local function CalcTurnCntr | Avinash James | 2.0 | 13-Jun-2016 |

| Added local function ProcTurnCntrReg. Added constants required for bitshifting and signal limiting. Added limiting block for output MotAg1TurnCntr. | Brendon Binder | 3.0 | 25-Aug-2017 |

| Update to FDD 4.1.0 added MotAg1WarnReg function | Mateusz Bartocha | 4.0 | 23-Oct-17 |

| Fix – Missed MotAg1TurnCntrRollgCntr output | Mateusz Bartocha | 5 | 21-Nov-17 |

| Updated Diagram & Unit Test Considerations | Matthew Leser | 6.0 | 14-Dec-2017 |

| Updated as per Design version 5.0.0 | Krzysztof Byrski | 7.0 | 25-Apr-2018 |

| Added ports for IO access | Avinash James | 8.0 | 27-Apr-2018 |

| Added updates for sensor offset learning | Avinash James | 9.0 | 04-May-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotAg1Meas High-Level Description6

3Design details of software module7

3.1Graphical representation of MotAg1Meas7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotAg1MeasInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.1.3Module Internal9

5.1.2Per: MotAg1MeasPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.1.3Per: MotAg1MeasPer29

5.1.3.1Design Rationale9

5.1.3.2Store Module Inputs to Local copies10

5.1.3.3(Processing of function)………10

5.1.3.4Store Local copy of outputs into Module Outputs10

5.2Server Runnables: MotAg1CoeffTblRead10

5.2.1.1Design Rationale10

5.2.1.2Store Module Inputs to Local copies10

5.2.1.3(Processing of function)………10

5.2.1.4Store Local copy of outputs into Module Outputs10

5.3Server Runnables: MotAg1CoeffTblWr10

5.3.1.1Design Rationale10

5.3.1.2Store Module Inputs to Local copies10

5.3.1.3(Processing of function)………10

5.3.1.4Store Local copy of outputs into Module Outputs10

5.4Server Runnables: MotAg1CfgLoPwrMod10

5.4.1.1Design Rationale10

5.4.1.2Store Module Inputs to Local copies10

5.4.1.3(Processing of function)………11

5.4.1.4Store Local copy of outputs into Module Outputs11

5.5Interrupt Functions11

5.6Module Internal (Local) Functions11

5.6.1ProcessErrorRegAndDieRevCtr11

5.6.2SPI_AnglePolarityAdjust11

5.6.3SPIvsENCA12

5.6.4CalcCorrnTbl12

5.6.5MotAgFaultProcessing12

5.6.6CalcNtcPrm13

5.6.7SetMotAg1FltNtc13

5.6.8OffsetCalculation14

5.6.9CalculateMotAgTurnCntr14

5.6.10SPI_AngleRawProcess15

5.6.11CompensateMechMtrPos15

5.7GLOBAL Function/Macro Definitions16

6Known Limitations with Design17

7UNIT TEST CONSIDERATION18

Appendix AAbbreviations and Acronyms19

Appendix BGlossary20

## Introduction

### Purpose

This document defines the module level design for the Sensor Offset and Correction Component. Major part of design has been captured in the FDD and any design rationale that has not been identified in the FDD and has been used to implement the component has been documented in the MDD

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## MotAg1MeasHigh-Level Description

The CDD_MotAg1Meas component is the complex driver for the motor angle 1 measurement subsystem.  This function initializes the registers for CSIH3 SPI channel for communicating with the motor angle 1 measurement sensor board. The SPI transmission is triggered periodically by DMA component.  This function receives the RAW sensor data at 62.5uS rate.  The component contains two source files, both described in this MDD:  CDD_MotAg1Meas.c contains the RTE runnables and services;  CDD_MotAg1Meas_MotCtrl.c  contains the motor control runnable.

.

## Design details of software module

See FDD.

### Graphical representation of MotAg1Meas

### Data Flow Diagram

See FDD.

#### Component level DFD

See FDD.

#### Function level DFD

See FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MOTAG1TURNCNTRLOLIM_CNT_F32 | Single point | Cnt | -256.09375 |

| MOTAG1TURNCNTRHILIM_CNT_F32 | Single point | Cnt | 255.96875 |

| MOTCTRLMOTAG1WARNREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG1WARNREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |

| MOTCTRLMOTAG1ERRREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG1ERRREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |

| MOTCTRLMOTAG1TURNCNTRREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG1TURNCNTRREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |



* Also see see FDD – CM640B_MotAg1Meas_DataDict.m file

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: MotAg1MeasInit1

### Design Rationale

All register initialization that is allowed at the register level (see Register/Field column of the CM640A_MotAg1Meas_RegisterConfiguration.xlsm spreadsheet in the FDD) is done at the register level to save execution time as compared to the read/modify/writes that would be needed to initialize at the field level.  Field level initialization done only where required by the spreadsheet.

### Module Outputs

See FDD: MotAg1MeasInit1 model block.

### Module Internal

See FDD: MotAg1MeasInit1 model block for Per Instance Memory.

#### Per: MotAg1MeasPer1

### Design Rationale

For run time efficiency in the motor control loop the Compensate MechMtrPos block is implemented in a optimized way in the code by letting a uint16 variable be overflown

### Store Module Inputs to Local copies

See FDD: MotAg1MeasPer1 model block

### (Processing of function)………

See FDD: MotAg1MeasPer1 model block.

### Store Local copy of outputs into Module Outputs

See FDD: MotAg1MeasPer1 model block.

#### Per: MotAg1MeasPer2

### Design Rationale

Details of the implementation of block “Process MotAg1RawErr” differ from the model in order to meet design and coding standards.

### Store Module Inputs to Local copies

See FDD: MotAg1MeasPer2 model block

### (Processing of function)………

See FDD: MotAg1MeasPer2 model block.

### Store Local copy of outputs into Module Outputs

See FDD: MotAg1MeasPer2 model block.

### Server Runnables: MotAg1CoeffTblRead

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg1CoeffTblRead block in the FDD

### Store Local copy of outputs into Module Outputs

None

### Server Runnables: MotAg1CoeffTblWr

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg1CoeffTblWr block in the FDD

### Store Local copy of outputs into Module Outputs

See MotAg1MeasMotAg1CoeffTblWrblock in the FDD

### Server Runnables: MotAg1CfgLoPwrMod

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg1CfgLoPwrMod block in the FDD

### Store Local copy of outputs into Module Outputs

See MotAg1CfgLoPwrMod block in the FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

#### ProcessErrorRegAndDieRevCtr



| Function Name | ProcessErrorRegAndDieRevCtr | Type 

*Body truncated: document is longer than the excerpt shown here.*
