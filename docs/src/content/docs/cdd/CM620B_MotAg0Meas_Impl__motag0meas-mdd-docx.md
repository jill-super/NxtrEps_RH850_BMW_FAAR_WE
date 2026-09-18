---
title: 'CM620B_MotAg0Meas_Impl — MotAg0Meas_MDD'
description: 'Converted Word (.docx) document MotAg0Meas_MDD.docx from module CM620B_MotAg0Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAg0Meas_MDD.docx` (Word (.docx), 170 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 3

## Converted content

Module Design Document

For

Motor Angle 0 Measurement

May 04, 2018

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

| Initial Version | Avinash James | 1.0 | 06-Jun-2016 |

| Removed local function CalcTurnCntr | Avinash James | 2.0 | 13-Jun-2016 |

| Updated as per Design version 2.0.0 | Krzysztof Byrski | 3.0 | 19-Oct-2017 |

| Updated as per Design version 5.0.0 | Krzysztof Byrski | 4.0 | 25-Apr-2018 |

| Updated the diagram for IO port additions | Avinash James | 5.0 | 27-Apr-2018 |

| Added updates for sensor offset learning | Avinash James | 6.0 | 04-May-2018 |



Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotAg0MeasHigh-Level Description6

3Design details of software module7

3.1Graphical representation of MotAg0Meas7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotAg0MeasInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.1.3Module Internal9

5.1.2Per: MotAg0MeasPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.1.3Per: MotAg0MeasPer29

5.1.3.1Design Rationale9

5.1.3.2Store Module Inputs to Local copies9

5.1.3.3(Processing of function)………10

5.1.3.4Store Local copy of outputs into Module Outputs10

5.1.4Per: MotAg0MeasPer310

5.1.4.1Design Rationale10

5.1.4.2Store Module Inputs to Local copies10

5.1.4.3(Processing of function)………10

5.1.4.4Store Local copy of outputs into Module Outputs10

5.2Server Runables: MotAg0CoeffTblRead10

5.2.1.1Design Rationale10

5.2.1.2Store Module Inputs to Local copies10

5.2.1.3(Processing of function)………10

5.2.1.4Store Local copy of outputs into Module Outputs10

5.3Server Runables: MotAg0CoeffTblWr10

5.3.1.1Design Rationale10

5.3.1.2Store Module Inputs to Local copies10

5.3.1.3(Processing of function)………10

5.3.1.4Store Local copy of outputs into Module Outputs11

5.4Interrupt Functions11

5.5Module Internal (Local) Functions12

5.5.1ProcessErrorRegAndDieRevCtr12

5.5.2SPI_AnglePolarityAdjust12

5.5.3SPIvsENCA12

5.5.4CalcCorrnTbl13

5.5.5MotAgFaultProcessing13

5.5.6CalcNtcPrm14

5.5.7SetMotAg0FltNtc14

5.5.8OffsetCalculation15

5.5.9CalculateMotAgTurnCntr15

5.5.10SPI_AngleRawProcess16

5.5.11CompensateMechMtrPos16

5.6GLOBAL Function/Macro Definitions17

6Known Limitations with Design18

7UNIT TEST CONSIDERATION19

Appendix AAbbreviations and Acronyms20

Appendix BGlossary21

Appendix CReferences22

## Introduction

### Purpose

This document defines the module level design for the Sensor Offset and Correction Component. Major part of design has been captured in the FDD and any design rationale that has not been identified in the FDD and has been used to implement the component has been documented in the MDD

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## MotAg0MeasHigh-Level Description

The CDD_MotAg0Meas component is the complex driver for the motor angle 1 measurement subsystem.  This function initializes the registers for CSIH3 SPI channel for communicating with the motor angle 1 measurement sensor board. The SPI transmission is triggered periodically by DMA component.  This function receives the RAW sensor data at 62.5uS rate.  The component contains two source files, both described in this MDD:  CDD_MotAg0Meas.c contains the RTE runnables and services;  CDD_MotAg0Meas_MotCtrl.c  contains the motor control runnable.

## Design details of software module

See FDD.

### Graphical representation of MotAg0Meas

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

| MOTAG0TURNCNTRLOLIM_CNT_F32 | Single point | Cnt | -256.09375 |

| MOTAG0TURNCNTRHILIM_CNT_F32 | Single point | Cnt | 255.96875 |

| MOTCTRLMOTAG0WARNREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG0WARNREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |

| MOTCTRLMOTAG0ERRREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG0ERRREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |

| MOTCTRLMOTAG0TURNCNTRREGLOLIM_CNT_U32 | 1 | Cnt | 0 |

| MOTCTRLMOTAG0TURNCNTRREGHILIM_CNT_U32 | 1 | Cnt | 67108863 |



* Also see FDD – CM620B_MotAg0Meas_DataDict.m file

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: MotAg0MeasInit1

### Design Rationale

All register initialization that is allowed at the register level (see Register/Field column of the CM620B_MotAg0Meas_RegisterConfiguration.xlsm spreadsheet in the FDD) is done at the register level to save execution time as compared to the read/modify/writes that would be needed to initialize at the field level.  Field level initialization done only where required by the spreadsheet.

### Module Outputs

See FDD: MotAg0MeasInit1 model block.

### Module Internal

See FDD: MotAg0MeasInit1 model block for Per Instance Memory.

#### Per: MotAg0MeasPer1

### Design Rationale

For run time efficiency in the motor control loop the Compensate MechMtrPos block is implemented in a optimized way in the code by letting a uint16 variable be overflown

### Store Module Inputs to Local copies

See FDD: MotAg0MeasPer1 model block

### (Processing of function)………

See FDD: MotAg0MeasPer1 model block.

### Store Local copy of outputs into Module Outputs

See FDD: MotAg0MeasPer1 model block.

#### Per: MotAg0MeasPer2

### Design Rationale

None

### Store Module Inputs to Local copies

See FDD: MotAg0MeasPer2 model block

### (Processing of function)………

See FDD: MotAg0MeasPer2 model block.

### Store Local copy of outputs into Module Outputs

See FDD: MotAg0MeasPer2 model block.

#### Per: MotAg0MeasPer3

### Design Rationale

None

### Store Module Inputs to Local copies

See FDD: MotAg0MeasPer3 model block

### (Processing of function)………

See FDD: MotAg0MeasPer3 model block.

### Store Local copy of outputs into Module Outputs

See FDD: MotAg0MeasPer3 model block.

### Server Runables: MotAg0CoeffTblRead

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg0CoeffTblRead block in the FDD

### Store Local copy of outputs into Module Outputs

None

### Server Runables: MotAg0CoeffTblWr

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg0CoeffTblWr block in the FDD

### Store Local copy of outputs into Module Outputs

See MotAg0MeasMotAg0CoeffTblWrblock in the FDD

### Server Runables: MotAg0CfgLoPwrMod

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

See MotAg0CfgLoPwrMod block in the FDD

### Store Local copy of outputs into Module Outputs

See MotAg0CfgLoPwrMod block in the FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

#### ProcessErrorRegAndDieRevCtr



| Function Name | ProcessErrorRegAndDieRevCtr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgErrReg_Cnt_T_u32 | uint32 | 0 | 67108863 |

|  | MotAgTurnCn

*Body truncated: document is longer than the excerpt shown here.*
