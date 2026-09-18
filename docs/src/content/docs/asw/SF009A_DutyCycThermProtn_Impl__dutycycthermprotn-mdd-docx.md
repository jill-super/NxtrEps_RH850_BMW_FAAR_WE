---
title: 'SF009A_DutyCycThermProtn_Impl — DutyCycThermProtn_MDD'
description: 'Converted Word (.docx) document DutyCycThermProtn_MDD.docx from module SF009A_DutyCycThermProtn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DutyCycThermProtn_MDD.docx` (Word (.docx), 156 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Sarika Natu', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 4 (png); OLE embeddings: 0; tables converted: 11

## Converted content

For

DutyCycThermProtn

Oct 26, 2017

Prepared By:

TATA ELXSI,

TRIVANDRUM, INDIA

Change History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sarika Natu(KPIT Technologies) | 1.0 | 02-Oct-2015 |

| Updated to version 2.0.0 of FDD | Krishna Anne | 2.0 | 07-Apr-2016 |

| Fix for anomaly EA4# 7558 | Krishna Anne | 3.0 | 29-Sep-2016 |

| Updated to FDD v3.0.0 | Shruthi Raghavan | 4.0 | 14-Dec-2016 |

| Updated as per FDD v4.0.0 | TATA | 5.0 | 25-Oct-2017 |



Table of Contents

1DutyCycThermProtn & High-Level Description5

2Design details of software module6

2.1Graphical representation of DutyCycThermProtn6

2.2Data Flow Diagram7

2.2.1Component level DFD7

2.2.2Function level DFD7

3Constant Data Dictionary8

3.1Program (fixed) Constants8

3.1.1Embedded Constants8

4Software Component Implementation9

4.1Sub-Module Functions9

4.1.1Init: DutyCycThermProtn_Init19

4.1.1.1Design Rationale9

4.1.1.2Module Outputs9

4.1.2Per: DutyCycThermProtn_Per19

4.1.2.1Design Rationale9

4.1.2.2Store Module Inputs to Local copies9

4.1.2.3(Processing of function)………9

4.1.2.4Store Local copy of outputs into Module Outputs9

4.2Server Runables9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.4.1Local Function #19

4.4.1.1Design Rationale9

4.4.1.2Processing10

4.4.2Local Function #210

4.4.2.1Design Rationale10

4.4.2.2Processing10

4.4.3Local Function #310

4.4.3.1Design Rationale10

4.4.3.2Processing10

4.4.4Local Function #410

4.4.4.1Design Rationale11

4.4.4.2Processing11

4.4.5Local Function #511

4.4.5.1Design Rationale11

4.4.5.2Processing11

4.4.6Local Function #611

4.4.6.1Design Rationale11

4.4.7Local Function #711

4.4.7.1Design Rationale12

4.4.8Local Function #812

4.4.8.1Design Rationale12

4.4.8.2Processing12

4.5GLOBAL Function/Macro Definitions12

5Known Limitations with Design13

6UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## DutyCycThermProtn & High-Level Description

The purpose of the Thermal Duty Cycle Protection is to limit and protect the system from excessive use, based on motor rotational velocity and system temperature. It also provides protection status information for use by other functions.

## Design details of software module

### Graphical representation of DutyCycThermProtn

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

Refer .m file



| Constant Name | Value |

| --- | --- |

| THERMLOADLIMSIZE_CNT_U08 | 8U |

| MULTFILTERSIZE_CNT_U08 | 6U |

| BITMASK2_CNT_U08 | 2U |

| BITMASK4_CNT_U08 | 4U |

| IDX5_CNT_U08 | 5U |

| IDX8_CNT_U08 | 8U |



## Software Component Implementation

### Sub-Module Functions

### Init: DutyCycThermProtn_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: DutyCycThermProtn_Per1

### Design Rationale

DutyCycThermProtn_Per1 function is divided into various functions to reduce the cyclomatic complexity.

The subsystems ‘Multiplier’ and ‘FilterPercMax’ are clubbed into ‘MultiFilterPercMax’ local function.

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



| Function Name | FiltSVReinit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IgnTiOff_Cnt_T_u32 | uint32 | 0 | 1720000 |

|  | VehTiVld_Cnt_T_Logl | Boolean | 0 | 1 |

| Return Value | None |  |  |  |



### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

### Local Function #2



| Function Name | TemperatureSelection | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsLimdTPrfmnc_Cnt_T_Logl | boolean | 0 | 1 |

|  | EcuTFild_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotFetT_DegCgrd_T_f32 | float32 | -50 | 200 |

|  | MotMagT_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotWidgT_DegCgrd_T_f32 | float32 | -50 | 300 |

|  | *Mult12Temp_DegCgrd_T_ s15p0 | Sint16 | -50 | 200 |

|  | *Mult36Temp_DegCgrd_T_s15p0 | Sint16 | -50 | 300 |

| Return Value | SlcTemp_DegCgrd_T_s15p0 | sint16 | -50 | 300 |



### Design Rationale

Name of local function matches with subsystem name from FDD

Note: The outputs of the function are Mult12Temp_DegCgrd_T_s15p0, Mult36Temp_DegCgrd_T_s15p0 and SlcTemp_DegCgrd_T_f32.

### Processing

None

### Local Function #3



| Function Name | TemperatureLimiting | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EcuTFild_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotWidgT_DegCgrd_T_f32 | float32 | -50 | 300 |

| Return Value | AbsTempLimitSlew_MotNwtMtr_T_f32 | float32 | 0 | 8.79 |



### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

None

### Local Function #4



| Function Name | MultiFilterPercMax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Mult12Temp_DegCgrd_T_s15p0 | sint16 | -50 | 200 |

|  | Mult36Temp_DegCgrd_T_s15p0 | sint16 | -50 | 300 |

|  | DutyCycThermProtnDi_Cnt_T_Logl | boolean | 0 | 1 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | MotCurrPeakEstimd_AmprSqd_T_f32 | float32 | 0 | 62500 |

|  | MotCurrPeakEstimdFild_AmprSqd_T_f32 | float32 | 0 | 62500 |

|  | *MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

| Return Value | ThermLimSlowFilMax_Uls_T_f32 | float32 | 0 | 200 |



### Design Rationale

The subsystems ‘Multiplier’ and ‘FilterPercMax’ are clubbed into ‘MultiFilterPercMax’ local function.

Note: The outputs of the function are MaxOut_Uls_T_u16p0 and ThermLimSlowFilMax_Uls_T_f32.

### Processing

None

### Local Function #5



| Function Name | ThermalLoadLimit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | SlcTemp_DegCgrd_T_s15p0 | sint16 | -50 | 300 |

|  | MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

| Return Value | ThermalLoadLmt_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |



### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

None

### Local Function #6



| Function Name | ThermalLimitStatus | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DutyCycThermProtnDi_Cnt_T_Logl | Boolean | 0 | 1 |

|  | MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

|  | ThermMotTqLim_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

| Return Value | ThermRednFac_Uls_T_f32 | float32 | 0 | 1 |



### Design Rationale

Name of local function matches with subsystem name from FDD. Initializing ThermRednFac_Uls_T_f32 to 0.0 helps to avoid writing another statement in the if-conditional (optimized compared to FDD)

### Local Function #7



| Function Name | TherrmalLimitScaling | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DualEcuFltMtgtnEna_Cnt_T_logl | Boolean | 0 | 1 |

|  | IvtrLoaMtgtnEna_Cnt_T_logl | Boolean | 0 | 1 |

|  | AbsTempLimitSlew_MotNwtMtr_T_f32 | float32 | 0 | 8.79 |

|  | DutyCycThermProtnDi_Cnt_T_Logl | Boolean | 0 | 1 |

|  | ThermalLoadLmt_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

|  | * ThermLoadDptLim_MotNwtMtr_T_f32 | Float32 | 0 | 8.8 |

|  | * ThermTempDptLim_MotNwtMtr_T_f32 | Float32 | 0 | 8.8 |

| Return Value | ThermMotTqLim_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |



### Design Rationale

Name of local function matches with subsystem name from FDD

The if-action subsystem blocks for calculation of LoadDptLim and TempDptLim are clubbed together and optimized since the condition for the subsystem execution was same.

### Local Function #8



| Function Name | UseInpLowr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | *TableX_Cnt_T_s16 | sint16 

*Body truncated: document is longer than the excerpt shown here.*
