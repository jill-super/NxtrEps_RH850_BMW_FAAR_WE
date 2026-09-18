---
title: 'RenesasMcalSuprt — Releasenotes_P1M-C_SPAL_R403_Ver4.02.00.D'
description: 'Converted PDF document Releasenotes_P1M-C_SPAL_R403_Ver4.02.00.D.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `Releasenotes_P1M-C_SPAL_R403_Ver4.02.00.D.pdf` (PDF, 797 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 55; title: Releasenotes_P1H-C_P1H-CE_FULL_R403_Ver4.01.00.001; author: REE

## Converted content

### Page 1

Renesas Electronics Release Date: 28/02/2017 
 
Page 1 of 55 
Release Notes for P1M-C-OpenMarket / 
RH850:RENESAS_SW-AUTOSAR-P1M-C: MCAL 
Ver4.02.00.D 
Beta Quality 
1.1 Purpose: 
To deliver AUTOSAR R4.0.3 MCAL software for P1x-C Ver4.02.00.D release using the following 
inputs. 
 
 Device Manual: r01uh0517ej0100_rh850p1x-c_Open.pdf 
 
 Device File: DF-RH850P1x-C-EE_E120b.zip 
 
 Operating Precautions: R01TU0087ED0101_RH850P1M-C.pdf 
 
 Modules supported: ADC, FLS, MCU, SPI and WDG. 
1.2 Package information 
Product RH850/P1x-C 
Variant P1M-C 
Product Release Version Ver4.02.00.D 
AUTOSAR Specification Version 4.0.3 
Devices supported RH850 
P1M-C – R7F701373, R7F701374 
Release Date 28-Feb-2017

### Page 2

Renesas Electronics Release Date: 28/02/2017 
 
Page 2 of 55 
1.3 Tools 
1.3.1 GHS 
Tool Version Options 
GreenHills 
Multi IDE – 
compiler 
Green Hills Multi 
V6.1.6 Compiler 
Version 2015.1.7 
 
-c -g -gsize -Wundef -Wshadow -nofloatio --short_enum 
--prototype_errors --diag_error 193 -dual_debug 
--no_commons -cpu=rh850g3m -Osize -prepare_dispose 
-inline_prologue -no_callt 
-ignore_callt_state_in_interrupts -sda=all -reserve_r2 
-large_sda -shorten_loads -shorten_moves -delete 
1.3.2 Configuration code generator 
Tool Version Options 
ECU Spectrum 4.0.14 - 
1.3.3 Additional software 
Tool Version Options 
NA - - 
 
 
1.4 Generic Information 
1.4.1 Release Target 
Processor P1M-C - R7F701373, R7F701374 
Module Generic 
Module Overview User Manual R20UT3827EJ0100-AUTOSAR.pdf – V1.0.2 
Getting Started for P1x-C MCAL User 
Manual 
R20UT3828EJ0100-AUTOSAR.pdf – V1.0.2 
Date 28-Feb-2017 
1.4.2 Release Items 
Filename Version Change Description 
Generator Files 
CommonHelper 0.0.3 Following changes are made in Ver4.02.00.D:- 
1. Updated macro IsBooleanParameterEnabledOrDisabled. 
2. Added macro IsBooleanNonMandateParameterEnabled. 
Common Files

### Page 3

Renesas Electronics Release Date: 28/02/2017 
 
Page 3 of 55 
ComStack_Types.h 1.0.0 No changes for release Ver4.02.00.D 
Std_Types.h 1.0.1 No changes for release Ver4.02.00.D 
rh850_Types.h 1.0.1 No changes for release Ver4.02.00.D 
Platform_Types.h 1.0.0 No changes for release Ver4.02.00.D 
Compiler Files 
Compiler.h 1.0.1 No changes for release Ver4.02.00.D 
Compiler_Cfg.h 1.0.1 No changes for release Ver4.02.00.D 
MemMap.h 1.0.2 Following changes are made in Ver4.02.00.D:- 
1. Memory section of modules MCU, SPI, WDG and FLS are 
updated. 
Os.h 1.0.1 No changes for release Ver4.02.00.D 
Os.c 1.0.0 No changes for release Ver4.02.00.D 
Getting Started for P1x-C MCAL User Manual 
R20UT3828EJ0100-AUTOSAR.pdf 1.0.2 Following changes are made in Ver4.02.00.D:- 
1. Added Section 4.10 – User Environment settings. 
2. Removed Description of Translation XML file from Chapter 
9 
3. Updated Copyright year 
4. Added example for reference in section 4.4 
5. In Chapter 4 Figure 4-2 has been updated as per version 
change 
6. Compiler Option Table updated 
7. In Chapter 5 Section 5.4.1 Trxml changed to Arxml format 
8. Chapter 9 Section 9.1 Configuration XML file remove since 
not relevant 
9. Document name corrected in second last and last page 
Module Overview User Manual 
R20UT3827EJ0100-AUTOSAR.pdf 1.0.2 Following changes are made in Ver4.02.00.D:- 
1. Updated section Configuration Parameter Dependency for 
GPT, ICU and PWM. 
2. Added Dem for ADC, PWM, PORT, DIO, SPI and GPT. 
3. Removed details regarding Dem from the section 3.1.16, 
ETH. 
4. Updated R number

### Page 4

Renesas Electronics Release Date: 28/02/2017 
 
Page 4 of 55 
1.4.3 Fixed Issues 
ID Description 
NA Please refer to the fixed issues list as shared from Renesas 
Ref. P1xC_FixedIssues_Ver4.02.00.D.xlsx 
1.4.4 Known Issues 
ID Description 
NA Please refer to the known issues list as shared from Renesas 
Ref. P1xC_OpenMarket_KnownIssues_CW09_2017.xlsx

### Page 5

Renesas Electronics Release Date: 28/02/2017 
 
Page 5 of 55 
1.5 Module Index 
 
2. ADC 
 
3. FLS 
 
4. MCU 
 
5. SPI 
 
6. WDG

### Page 6

Renesas Electronics Release Date: 28/02/2017 
 
Page 6 of 55 
2 ADC 
2.1 Target Info 
Processor P1M-C - R7F701373, R7F701374 
Module ADC 
Software Version V1.0.1 
Embedded User Manual R20UT3635EJ0100-AUTOSAR.pdf– V1.0.2 
Tool User Manual R20UT3636EJ0100-AUTOSAR.pdf – V1.0.2 
Date 28-Feb-2017 
 
2.2 Release Items 
Filename Version Change Description 
P1x-C - Parameter Definition files 
R403_ADC_P1X-C.arxml 1.0.1 Following changes are made in Ver4.02.00.D:- 
1. Added Dem parameters ADC_E_DMA_FAILURE, 
ADC_E_INT_INCONSISTENT & 
ADC_E_REG_WRITE_VERIFY . 
2. Added parameters AdcEnableSelfDiag, AdcEnableAdTimer, 
AdcEnableBufferAllocation, AdcInterruptConsistencyCheck, 
AdcWriteVerify, AdcDmacWriteVerify, AdcPic2cWriteVerify, 
AdcPullDownPulseWidth, AdcUlmtLlmtErrIntEnable, 
AdcEnableAdTimerTriggMode, AdcTimerPeriod, 
AdcTimerPhaseDelay, AdcIdErrIntEnable, 
AdcParityErrIntEnable. 
3. Modified parameter AdcSelfDiagMode. 
4. Updated description of AdcChannelRangeSelect, 
AdcEnableChSelfDiag, AdcSelfDiagConvCktRef, 
AdcEnablePullUpPullDown, AdcSelfDiagPinLevel. 
5. Max value of parameters AdcChannelConvTime, 
AdcChannelResolution, AdcChannelSampTime and 
AdcHwTrigTimer updated. 
6. Upper Multiplicity of AdcExtMuxValue and 
AdcExtMuxDelayCounter modified. 
7. Modified LITERALS of AdcSelfDiagConvCktRef. 
8. Added DOC-REVISION in ADMIN-DA TA. 
9. Removed parameter AdcHwUnitMaxChannelId, 
AdcHwUnitTotalConvTime. 
10. Copy right information updated.

### Page 7

Renesas Electronics Release Date: 28/02/2017 
 
Page 7 of 55 
11. Limit check option 'ADC_RANGE_NOT_BETWEEN' is 
removed from the parameter 'AdcChannelRangeSelect'. 
12. Support for device R7F701371 added. 
13. Added parameter AdcWriteVerifyErrorInterface. 
14. As per ARDAAAF-1363, Warranty Disclaimer updated 
15. Removed literals ADTIM3_SG3_SG4 and 
ADTIM4_SG3_SG4 from parameter AdcHwTrigger. 
BSWMDT 
R403_ADC_P1x-C_BSWMDT.arx
ml 
1.0.2 Following changes are made in Ver4.02.00.D:- 
1. CAN-ENTER-EXCLUSIVE-AREA-REF tag is added. 
2. Warranty Disclaimer updated. 
3. Software patch version incremented. 
Source Code 
Adc.c 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
Adc_Irq.c 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
Adc_Private.c 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x V4.01.01 branch. 
2. PIC register implementation modified. 
3. Copyright information updated. 
4. Comments added for traceability. 
5. Removed Misra warning Msg(4:2892) from MISRA C Rule 
Violations. 
6. Added volatile to LpRunTimeData in APIs 
Adc_GroupCompleteMode, 
Adc_ConfigureGroupForConversion, 
Adc_HwEnableHardwareTrigger and Adc_ProcessQueue. 
Adc_Ram.c 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x branch. 
2. Added volatile to Adc_GpRunTimeData. 
3. Copyright information updated. 
Adc_Version.c 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x branch. 
2. Copyright information updated.

### Page 8

Renesas Electronics Release Date: 28/02/2017 
 
Page 8 of 55 
Adc.h 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x V4.01.01 branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
Adc_Debug.h 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x V4.01.01 branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
Adc_Irq.h 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x V4.01.01 branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
Adc_PBTypes.h 2.0.0 Following changes are made in Ver4.02.00.D:- 
1. File adapted from P1x V4.01.01 branch. 
2. Copyright information updated. 
3. Comments added for traceability. 
4. Removed variable blExtMuxEnabled

*Excerpt: first 8 of 55 pages shown.*
