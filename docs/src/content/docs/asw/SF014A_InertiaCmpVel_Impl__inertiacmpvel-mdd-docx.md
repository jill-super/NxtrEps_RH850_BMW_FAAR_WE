---
title: 'SF014A_InertiaCmpVel_Impl — InertiaCmpVel_MDD'
description: 'Converted Word (.docx) document InertiaCmpVel_MDD.docx from module SF014A_InertiaCmpVel_Impl.'
sidebar:
  hidden: true
---

> **Source:** `InertiaCmpVel_MDD.docx` (Word (.docx), 157 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 4 (emf, png); OLE embeddings: 1; tables converted: 11

## Converted content

For

InertiaCmpVel

August 18, 2017

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USAChange History



| SNo | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1.0 | 23-Jul-2015 |

| 2 | Updated to version 1.3.0 of design | SB | 2.0 | 11-Mar-2016 |

| 3 | Updated to version 1.7.0 and 1.8.0 of design | KK | 3.0 | 21-Jun-2016 |

| 4 | Updated to version 1.9.0 of design | KK | 4.0 | 14-Jul-2016 |

| 5 | Updated Graph and function input | ML | 5.0 | 18-Aug-2017 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2InertiaCmpVel & High-Level Description5

3Design details of software module6

3.1Graphical representation of InertiaCmpVel6

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1.1Sub-Module Functions9

5.1.2Interrupt Service Routines9

5.1.3Server Runnable Functions9

5.1.4Module Internal (Local) Functions9

5.1.5Transition Functions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## InertiaCmpVel & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of InertiaCmpVel

### Data Flow Diagram

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

None

#### Global Constants

Refer .m file

#### User defined typedef definition/declaration

This section documents any user types uniquely used for the module.



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| typedef struct FilCoeffRec | b0_Uls_f32 | Float32 | FULL | FULL |

|  | b1_Uls_f32 | Float32 | FULL | FULL |

|  | b2_Uls_f32 | Float32 | FULL | FULL |

|  | a0_Uls_f32 | Float32 | FULL | FULL |

|  | a1_Uls_f32 | Float32 | FULL | FULL |

|  | a2_Uls_f32 | Float32 | FULL | FULL |



## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module InertiaCmpVelInit1()

Design Rational:

Init function is not present in the model but in reference to the Init.txt  text file Low pass filter and Notch filter are initialized.

For Low pass filter standard EA4 LPF implementation from NxtrFil.h is followed and for Notch filter initialization, EA3 implementation is followed.

#### Periodic sub-module InertiaCmpVelPer1()

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Calculate Driver Velocity



| Function Name | DrvrVelCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

| Return Value | ScadDrvrVel_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |



#### Calculate ADD Coefficient



| Function Name | ADDCoeffCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AssiCmdBas_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | WhlImbRejctnAmp_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

| Return Value | ADDCoeffCalc_MotNwtMtrSpRad_T_f32 | float32 | 0.0 | 0.00007 |



#### Calculate Gain



| Function Name | DecelGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLgtA_KphPerSec_T_f32 | float32 | -35 | 35 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | DecelGain_Uls_T_f32 | float32 | 0 | 1 |



#### Calculate Filter Coefficients



| Function Name | FilCoeffCalc | Type | Min | Max |  |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | ADDCoeff_MotNwtMtrPerMotRadPerSec_T_f32 | float32 | 0.0 | 0.041306 |  |

|  | WhlImbRejctnAmp_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |  |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |  |

| Return Value | *FilCoeff_T_Rec | b0_Uls_f32 | float32 | -2.74156205240179 | 0 |

|  |  | b1_Uls_f32 | float32 | 0.0 | 0.330448 |

|  |  | b2_Uls_f32 | float32 | -0.160083862455113 | 2.41111405240179 |

|  |  | a0_Uls_f32 | float32 | 0.5525885 | 3.9498924 |

|  |  | a1_Uls_f32 | float32 | -7.9996842 | -4.8417266 |

|  |  | a2_Uls_f32 | float32 | 4.0504234 | 10.6056849 |



#### Generate Command



| Function Name | GenFddIcCmd | Type | Min | Max |  |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | ScadDrvrVel_MotRadPerSec_T_f32 | float32 | -7226.652 | 7226.652 |  |

|  | *FilCoeff_T_Rec | b0_Uls_f32 | float32 | -2.74156205240179 | 0 |

|  |  | b1_Uls_f32 | float32 | 0.0 | 0.330448 |

|  |  | b2_Uls_f32 | float32 | -0.166262133009164 | 2.41111405240179 |

|  |  | a0_Uls_f32 | float32 | 0.5525885 | 3.9498924 |

|  |  | a1_Uls_f32 | float32 | -7.9996842 | -4.8417266 |

|  |  | a2_Uls_f32 | float32 | 4.0504234 | 10.6056849 |

| Return Value | InertiaCmp_MotNwtMtr_T_f32 | Float | -8.8 | 8.8 |  |



#### NotchCmp



| Function Name | NotchCmp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | InertiaCmp_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | WhlImbRejctnAmp_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

| Return Value | NotchCmp _MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |



#### FilNotchFullUpdOutp_f32



| Function Name | FilNotchFullUpdOutp_f32 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | None |  |  |  |



#### Description

Notch filter output calculation implemented based on ‘Inertia Comp Notch’ block functionality.

#### FilNotchInit



| Function Name | FilNotchInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | FilOut | float32 |  |  |



#### Description

Notch filter initialization function implemented based on EA3 design.

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

- Since the notch filter implementation used in this module is dynamic in nature, absolute ranges are difficult to determine without pre-defined knowledge on the combination of coefficient values (A1, A2, B0, B1, B2).  Because of this, the systems group ran simulations on 10 different combinations of coefficients (2 with defined default calibrations, 8 considered extreme cases of notch filters) and logged the ranges of the filter state variables and outputs during a frequency sweep.  The ranges given throughout this module were taken as the worst case results of all of the given test cases.

To provide useful cases for unit testing, the boundary checks tested during unit testing should be altered to test the state variable minimum and maximum for each of the 10 test cases with the given coefficients set to the values given in that test case.  In the case where the default values of the coefficients are used in a vector, the unit tester should not test the corresponding state variables with values over the range defined for that set of coefficients.  See attached simulation results.

- GenFddIcCmd function is designed to work with argument values from the calling function as used with the other functions in the module, and outputs may be out of the expected range if tested with arbitrary combinations of input values.  Unit testing of this function should use only passed argument value combinations coming from the calling function.

#### Abbreviations and Acronyms



| Abbrevi

*Body truncated: document is longer than the excerpt shown here.*
