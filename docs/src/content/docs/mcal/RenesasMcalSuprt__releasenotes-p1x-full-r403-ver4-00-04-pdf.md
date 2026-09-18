---
title: 'RenesasMcalSuprt — Releasenotes_P1x_FULL_R403_Ver4.00.04'
description: 'Converted PDF document Releasenotes_P1x_FULL_R403_Ver4.00.04.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `Releasenotes_P1x_FULL_R403_Ver4.00.04.pdf` (PDF, 602 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 42; title: 1; author: REE

## Converted content

### Page 1

Renesas Electronics Release Date: 08/06/2015 
 
Page 1 of 42 
Release Notes for RENESAS RH850/P1x: 
RENESAS_SW-AUTOSAR-P1x: MCAL Ver4.00.04 
QM Beta Quality 
1.1 Purpose: 
To deliver AUTOSAR R4.0.3 MCAL software for P1x V4.00.04 release using the following inputs. 
 
 Device Manual: r01uh0436ej0070_rh850p1x.pdf 
 
 Device File: DF-RH850P1M-EE_V100.zip 
 
 Operating Precautions: R01TU0069ED0200_RH850.pdf 
 
 Flash Libraries: RENESAS_FCL_RH850_T01E_V2.00.exe 
 RENESAS_FDL_RH850_T01E_V2.00.exe 
 
 Modules supported: ADC, CAN, DIO, FLS, FLSTST, FR, GPT, ICU, MCU, PORT, PWM, 
 RAMTST, SPI, WDG.

### Page 2

Renesas Electronics Release Date: 08/06/2015 
 
Page 2 of 42 
1.2 Package information 
Product RH850/P1x 
Variant P1M 
Product Release Version Ver4.00.04 
AUTOSAR Specification Version 4.0.3 
Device tested on P1M - R7F701310 
Devices supported R7F701304 
R7F701305 
R7F701310 
R7F701311 
R7F701312 
R7F701313 
R7F701314 
R7F701315 
R7F701318 
R7F701319 
R7F701320 
R7F701321 
R7F701322 
R7F701323 
Release Date 08-June-2015

### Page 3

Renesas Electronics Release Date: 08/06/2015 
 
Page 3 of 42 
1.3 Tools 
1.3.1 GHS 
Tool Version Options 
GreenHills 
Multi IDE – 
compiler 
Green Hills Multi 
V6.1.4 Compiler 
Version 2013.5.5 
+ 
Patches : 
P2, P9, P12, P13, 
P14 
-Ospace -g -cpu=rh850g3k -gsize 
-prepare_dispose -sda=all -passsource 
-Wundef -no_callt -reserve_r2 
--short_enum -fsoft --prototype_errors 
--diag_error 193 -dual_debug -large_sda 
--no_commons -shorten_loads 
-shorten_moves -Wshadow -nofloatio 
-ignore_callt_state_in_interrupts -delete 
-inline_prologue 
1.3.2 Configuration code generator 
Tool Version Options 
ECU Spectrum 4.0.14 - 
1.3.3 Additional software 
Tool Version Options 
NA - -

### Page 4

Renesas Electronics Release Date: 08/06/2015 
 
Page 4 of 42 
1.4 Generic Information 
1.4.1 Release Target 
Processor P1M - R7F701310 
Module Generic 
Date 08-June-2015 
1.4.2 Release Items 
Filename Version Change Description 
P1x_translation.h 1.0.6 File updated for FLS and CAN macros. 
ComStack_Types.h 1.0.1 No change 
Std_Types.h 1.0.1 No change 
rh850_Types.h 1.0.4 No change 
Platform_Types.h 1.0.1 No change 
Compiler.h 1.0.3 No change 
Compiler_Cfg.h 1.0.5 No change 
MemMap.h 1.0.6 No change 
NvM_Types.h 1.0.1 No change 
Os.h 1.0.1 No change 
Os.c 1.0.2 No change 
GettingStarted_MCAL_Drivers_X1x.
pdf 
1.0.5 No change 
AUTOSAR_Modules_Overview.pdf 1.0.7 No change 
1.4.3 Known Issues 
ID Description 
1. Please refer KnownIssues_P1x_R403_2015_CW23.pdf

### Page 5

Renesas Electronics Release Date: 08/06/2015 
 
Page 5 of 42 
 
1.5 Module Index 
 
ADC 
 
CAN 
 
DIO 
 
FLS 
 
FLSTST 
 
FR 
 
GPT 
 
ICU 
 
MCU 
 
PORT 
 
PWM 
 
RAMTST 
 
SPI 
 
WDG

### Page 6

Renesas Electronics Release Date: 08/06/2015 
 
Page 6 of 42 
2 ADC 
2.1 Target Info 
Processor P1M - R7F701310 
Module ADC 
Date 08-June-2015 
2.2 Release Items 
Filename Version Change Description 
P1x- Parameter Definition files 
R403_ADC_P1M_04_05_12_13_20
_21.arxml 
1.0.5 As part of Px4 V4.00.04 Release, following changes 
are made 
1. As per mantis #24237, Parameter 
AdcUseHwContiScanMode is added in AdcGroup container. 
2. As per mantis #27411, PDF name is modified. 
3. Copyright information is updated. 
R403_ADC_P1M_10_11_14_15_18
_19_22_23.arxml 
1.0.6 As part of Px4 V4.00.04 Release, following changes 
are made 
1. As per mantis #24237, Parameter 
AdcUseHwContiScanMode is added in AdcGroup container. 
2. As per mantis #27411, PDF name is modified. 
3. Copyright information is updated. 
BSWMDT 
R403_ADC_P1x_BSWMDT.arxml 1.0.4 As part of P1x V4.00.04 Release, following changes are made: 
1. Software version is updated. 
2. As per mantis #26305, critical section name 
'RAMDA TA_PROTECTION' is changed to 
'ADC_RAMDA TA_PROTECTION'. 
3. Copyright information is updated. 
Source Code 
Adc.c 1.7.7 As part of P1x V4.00.04 Release, following changes are made: 
1. NULL check is added for 'PtrToSamplePtr' in 
Adc_GetStreamLastPointer() API. 
2. As per mantis #26305, critical section name 
'RAMDA TA_PROTECTION' is changed to 
'ADC_RAMDA TA_PROTECTION'. 
3. MISRA violation is updated. 
Adc_Irq.c 1.3.4 No change

### Page 7

Renesas Electronics Release Date: 08/06/2015 
 
Page 7 of 42 
Adc_Private_ADCD_ADCB.c 1.0.7 As part of P1x V4.00.04 Release, following changes are made: 
1. As per mantis #24936 Redundant compilation switches are 
corrected in Adc_GroupCompleteMode() API. 
2. As per mantis #25801, 'Track and Hold' implementation is 
corrected to match with the flow diagram in the HW User 
manual. 
3. As per mantis #26305, critical section name 
'RAMDA TA_PROTECTION' is changed to 
'ADC_RAMDA TA_PROTECTION'. 
4. As per mantis #25842, position of critical section exit is 
corrected in Adc_GroupCompleteMode API. 
5. As per mantis #24237, software re-triggering is implemented 
for continuous conversion for software triggered groups. 
6. As per mantis #27488, HW triggered One-shot conversion is 
corrected to avoid conversion of more than one stream in one 
HW trigger. 
7. As per mantis #26324, volatile declaration is added for 
variables storing register values. 
8. MISRA violation is updated. 
9. As per mantis #27334, redundant variables and double 
assignments are removed. 
10. As per mantis #27186, index calculation of the array 
'Adc_GpRunTimeData' is corrected to avoid out of bound 
access. 
Adc_Ram.c 1.5.3 No change 
Adc_Version.c 1.1.3 No change 
Adc.h 1.5.5 No change 
Adc_Debug.h 1.0.2 No change 
Adc_Irq.h 1.0.9 No change 
Adc_PBTypes_ADCD_ADCB.h 1.0.5 As part of P1x V4.00.04 Release, following changes are made: 
1. As per mantis #25801, 'Track and Hold' implementation is 
corrected to match with the flow diagram in the HW Usermanual. 
2. As per mantis #26331, element names are corrected in union 
'UInt'. 
3. As per mantis #26324, volatile declaration is added for 
variables storing register values. 
Adc_Private.h 1.4.6 As part of P1x V4.00.04 Release, following changes are made: 
1.

### Page 8

Renesas Electronics Release Date: 08/06/2015 
 
Page 8 of 42 
Adc_Ram.h 1.5.3 No change 
Adc_Types.h 1.7.4 No change 
Adc_Version.h 1.1.1 No change 
Tool Executable 
Adc_ADCD_ADCB.exe 1.3.2 Tool exe updated for tool code changes. 
Adc_ADCD_ADCB.cfgxml 1.0.1 No change 
X1x Common Sample Application Source file 
App_ADC_Common_Sample.c 1.1.9 No change for P1x V4.00.04 release. 
X1x Common Sample Application Header file 
App_ADC_Common_Sample.h 1.0.4 No change for P1x V4.00.04 release. 
P1x Sample Application P1M Source file 
App_ADC_P1M_Sample.c 1.0.1 No change for P1x V4.00.04 release. 
P1x Sample Application P1M Header file 
App_ADC_Device_Sample.h 1.0.2 No change for P1x V4.00.04 release. 
P1x User Manual 
AUTOSAR_ADC_Component_Use
rManual.pdf 
1.0.4 The following changes are done. 
1. Chapter 2 is updated for reference document. 
2. Section 3.1 is updated for folder section. 
3. Section 4.1 is updated for usage guidelines. 
4. In chapter 13, P1M supported devices are added. 
5. Section 13.1 is updated for translation header file and 
parameter definition files. 
6. Section 13.2 is updated for sample application structure and 
building sample application. 
7. Section 13.3 is updated for memory and throughput details. 
8. Chapter 14 is updated for version of ADC Driver component. 
9. Range of ChannelId is corrected in sections 10.3.1 and 10.3.2. 
10. Channel Mapping is corrected in section 10.3.3. 
11. Table 13-2 is updated for CAT-2 ERROR ISR. 
AUTOSAR_ADC_Tool_UserManu
al.pdf 
1.0.4 1. Error message ERR123140 is added. 
2. Section 2.1 Reference Documents are updated to add PDF 
reference. 
3. List of mandatory parameters is updated in section 8.1. 
2.3 Known Issues 
ID Description 
1. Please refer KnownIssues_P1x_R403_2015_CW23.pdf

*Excerpt: first 8 of 42 pages shown.*
