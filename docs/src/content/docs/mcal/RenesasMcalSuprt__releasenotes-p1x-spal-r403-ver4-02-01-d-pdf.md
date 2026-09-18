---
title: 'RenesasMcalSuprt — Releasenotes_P1x_SPAL_R403_Ver4.02.01.D'
description: 'Converted PDF document Releasenotes_P1x_SPAL_R403_Ver4.02.01.D.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `Releasenotes_P1x_SPAL_R403_Ver4.02.01.D.pdf` (PDF, 562 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 32; title: Releasenotes_P1x_SPAL_R403_Ver4.02.01.D; author: REE

## Converted content

### Page 1

Renesas Electronics Release Date: 24/02/2017 
 
Page 1 of 32 
Release Notes for RENESAS RH850/P1x: 
RENESAS_SW-AUTOSAR-P1x: MCAL Ver4.02.01.D 
MP Quality 
1.1 Purpose: 
To deliver AUTOSAR R4.0.3 MCAL software for P1x Ver4.02.01.D release using the following 
inputs. 
 
 Device Manual: r01uh0436ej0130-rh850p1x.pdf 
 
 Device File: DF-RH850P1M-EE_V120.zip 
 
 Operating Precautions: R01TU0069ED0300_RH850.pdf 
 
 Modules supported: DIO, FLS, MCU, PORT, SPI and WDG. 
 
 
 
 
 
 
 
 
Note: In case of integration of this product into safety related applications please contact Renesas for 
additional safety related work products.

### Page 2

Renesas Electronics Release Date: 24/02/2017 
 
Page 2 of 32 
1.2 Package information 
Product RH850/P1x 
Variant P1M 
Product Release Version Ver4.02.01.D 
AUTOSAR Specification Version 4.0.3 
Device tested on P1M - R7F701318 
P1M - R7F701310 
Devices supported RH850/P1M 
R7F701310 
R7F701311 
R7F701314 
R7F701315 
R7F701318 
R7F701319 
R7F701322 
R7F701323 
Release Date 24-Feb-2017 
 
Additional to the above list, the following derivatives (with ICU-S units) are also supported: 
 
ICU-S Devices supported R7F701362 
R7F701363 
R7F701366 
R7F701367 
 
As there was no impact on MCAL identified due to the ICU-S unit, Renesas recommends to use the below equivalent 
devices part number without ICU-S unit, during MCAL configuration, instead of the actual device part number with 
ICU-S unit: 
 
Device (with ICU-S Support) Equivalent device(w/o ICU-S support) 
R7F701362 R7F701318 
R7F701363 R7F701319 
R7F701366 R7F701322 
R7F701367 R7F701323

### Page 3

Renesas Electronics Release Date: 24/02/2017 
 
Page 3 of 32 
1.3 Tools 
1.3.1 GHS 
Tool Version Options 
GreenHills 
Multi IDE – 
compiler 
Green Hills Multi 
V6.1.6 Compiler 
Version 2015.1.7 
 
-c -Osize -g -cpu=rh850g3m -gsize -prepare_dispose 
-inline_prologue -sda=all -Wundef -no_callt -reserve_r2 
--short_enum --prototype_errors --diag_error 193 
-dual_debug -large_sda --no_commons -shorten_loads 
-shorten_moves -Wshadow -nofloatio 
-ignore_callt_state_in_interrupts -delete 
1.3.2 Configuration code generator 
Tool Version Options 
ECU Spectrum 4.0.14 - 
1.3.3 Additional software 
Tool Version Options 
NA - - 
 
1.4 Generic Information 
1.4.1 Release Target 
Processor P1M - R7F701318 
Module Generic 
Module Overview User Manual R20UT3752EJ0101-AUTOSAR.pdf – V1.0.10 
Getting Started for P1x MCAL User 
Manual 
R20UT3753EJ0101-AUTOSAR.pdf – V1.0.8 
Date 24-Feb-2017 
1.4.2 Release Items 
Filename Version Change Description 
Generator Files 
P1x_translation.h 1.0.8 Following changes are made in Ver4.02.01.D: 
1. Updated supported devices list in 'Environment'. 
2. Updated copyright information. 
Common Files 
ComStack_Types.h 1.0.1 No changes for release Ver4.02.01.D 
Std_Types.h 1.0.1 No changes for release Ver4.02.01.D

### Page 4

Renesas Electronics Release Date: 24/02/2017 
 
Page 4 of 32 
rh850_Types.h 1.0.4 No changes for release Ver4.02.01.D 
Platform_Types.h 1.0.1 No changes for release Ver4.02.01.D 
Compiler Files 
Compiler.h 1.0.5 No changes for release Ver4.02.01.D 
Compiler_Cfg.h 1.0.5 No changes for release Ver4.02.01.D 
MemMap.h 1.0.10 Following changes are made in Ver4.02.01.D:- 
1. Copyright information is updated. 
2. Memory section 
FLS_START_SEC_PRIV A TERAM_CODE and 
FLS_STOP_SEC_PRIV A TERAM_CODE added for FLS 
module. 
Os.h 1.0.1 No changes for release Ver4.02.01.D 
Os.c 1.0.2 No changes for release Ver4.02.01.D 
RUCG Tool 
RUCG.exe 1.1 No changes for release Ver4.02.01.D 
 
Getting Started for P1x MCAL User Manual 
R20UT3753EJ0101-AUTOSAR.pdf 1.0.8 Following changes are made in Ver4.02.01.D:- 
1. Added R-number. 
2. Updated Notice and copyright information. 
Module Overview User Manual 
R20UT3752EJ0101-AUTOSAR.pdf 1.0.10 Following changes are made in Ver4.02.01.D:- 
1. New section 3.4 added for Deviation List. 
2. Updated section 3.2 ‘RH850 Macros Definition’ for adding 
explanation regarding usage and modification of macros. 
3. Updated R-Number. 
4. Updated notice and copyright information. 
5. Removed 3.2.2 related information from Chapter 2 
‘Reference Documents’ and ‘Definitions’. 
6. Corrected page numbers 
RUCG Tool User Manual 
R20UT3754EJ0101-AUTOSAR.pdf 1.1.3 Following change is made in Ver4.02.01.D:- 
1. Updated notice and copyright information. 
2. Updated R Number.

### Page 5

Renesas Electronics Release Date: 24/02/2017 
 
Page 5 of 32 
1.4.3 Fixed Issues 
ID Description 
NA Please refer to the fixed issues list as shared from Renesas 
Ref. P1M_FixedIssues_Ver4.02.01.D.xlsx. 
1.4.4 Known Issues 
ID Description 
NA Please refer to the known issues list as shared from Renesas 
Ref. P1M_KnownIssues_QM_CW08_2017.xlsx.

### Page 6

Renesas Electronics Release Date: 24/02/2017 
 
Page 6 of 32 
1.5 Module Index 
 
DIO 
 
FLS 
 
MCU 
 
PORT 
 
SPI 
 
WDG

### Page 7

Renesas Electronics Release Date: 24/02/2017 
 
Page 7 of 32 
2 DIO 
2.1 Target Info 
Processor P1M - R7F701318 
Module DIO 
Software Version 1.0.12 
Embedded User Manual R20UT3708EJ0101-AUTOSAR.pdf – V1.0.10 
Tool User Manual R20UT3709EJ0101-AUTOSAR.pdf – V1.0.6 
Date 24-Feb-2017 
2.2 Release Items 
Filename Version Change Description 
P1x- Parameter Definition files 
R403_DIO_P1M_04_05_12_13_20_
21.arxml 
1.0.6 Following changes are made in Ver4.02.01.D:- 
1. For Requirement TPS_ECUC_06004, ADMIN-DA TA 
section is updated. 
2. Updated Copyright information. 
R403_DIO_P1M_10_11_14_15_18_
19_22_23.arxml 
1.0.7 Following changes are made in Ver4.02.01.D:- 
1. For Requirement TPS_ECUC_06004, ADMIN-DA TA 
section is updated. 
2. Updated Copyright information. 
BSWMDT 
R403_DIO_P1x_BSWMDT.arxml 1.0.7 Following changes are made in Ver4.02.01.D:- 
1. Corrected Service ID of API Dio_Init to decimal value. 
2. Copyright information is updated. 
3. Software patch version is updated. 
Source Code 
Dio.c 1.0.24 Following changes are made in Ver4.02.01.D:- 
1. Removed unnecessary Requirement tag 
'EAAR_PN0034_FR_0017' and corrected requirement 
'DIO140' in Dio_WritePort. 
2. Copyright information is updated. 
3. Added inclusion of "Dio_RegWrite.h". 
Dio_Ram.c 1.0.9 No changes for release Ver4.02.01.D 
Dio_Version.c 1.0.7 No changes for release Ver4.02.01.D 
Dio.h 1.0.14 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Inclusion of "Dio_RegWrite.h" is removed and numeric

### Page 8

Renesas Electronics Release Date: 24/02/2017 
 
Page 8 of 32 
values are appended with 'U' for macro definitions. 
3. Copyright information is updated. 
Dio_Debug.h 1.0.5 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Copyright information is updated. 
Dio_PBTypes.h 1.0.15 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Numeric values are appended with 'U' for macro 
definitions. 
3. Copyright information is updated. 
Dio_Ram.h 1.0.13 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Copyright information is updated 
Dio_RegWrite.h 1.0.1 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Copyright information 'Copyright(c) 2017' corrected to 
'Copyright(c) 2016-2017'. 
3. Removed macro 'DIO_DEM_TYPE' 
Dio_Version.h 1.0.10 Following changes are made in Ver4.02.01.D:- 
1. Requirement tag 'implements' changed to 'DIO_H_00x :'. 
2. Included "Dem.h" file. 
3. Copyright information is updated. 
DLL executable code for DIO configuration generation 
Dio_X1x.dll 1.0.19 Following change is made in Ver4.02.01.D:- 
1. Tool .dll updated for tool code changes. 
Dio_X1x.cfgxml 1.0.2 Following changes are made in Ver4.02.01.D:- 
1. A new filter option, <FILTER-RENESAS> is added to 
handle multiple module instances 
2. Copyright information updated 
P1x Sample Application P1M Source file 
App_DIO_P1M_Sample.c 1.0.7 Following cha

*Excerpt: first 8 of 32 pages shown.*
