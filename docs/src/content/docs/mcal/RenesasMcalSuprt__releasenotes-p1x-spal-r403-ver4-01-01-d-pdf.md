---
title: 'RenesasMcalSuprt — Releasenotes_P1x_SPAL_R403_Ver4.01.01.D'
description: 'Converted PDF document Releasenotes_P1x_SPAL_R403_Ver4.01.01.D.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `Releasenotes_P1x_SPAL_R403_Ver4.01.01.D.pdf` (PDF, 797 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 56; title: Releasenotes_P1x_SPAL_R403_Ver4.01.01.D; author: REE

## Converted content

### Page 1

Renesas Electronics Release Date: 31/10/2016 
 
Page 1 of 56 
Release Notes for RENESAS RH850/P1x: 
RENESAS_SW-AUTOSAR-P1x: MCAL Ver4.01.01.D 
Beta Quality 
1.1 Purpose: 
To deliver AUTOSAR R4.0.3 MCAL software for P1x Ver4.01.01.D release using the following 
inputs. 
 
 Device Manual: r01uh0436ej0111_rh850p1x.pdf 
 
 Device File: DF-RH850P1M-EE_V120.zip 
 
 Operating Precautions: R01TU0069ED0300_RH850.pdf 
 
 Modules supported: DIO, FLS, MCU, PORT, SPI and WDG.

### Page 2

Renesas Electronics Release Date: 31/10/2016 
 
Page 2 of 56 
1.2 Package information 
Product RH850/P1x 
Variant P1M 
Product Release Version Ver4.01.01.D 
AUTOSAR Specification Version 4.0.3 
Device tested on P1M - R7F701310 
Devices supported RH850/P1M 
R7F701304 
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
Release Date 31-Oct-2016 
 
Additional to the above list, the following derivatives (with ICU-S units) are also supported: 
 
ICU-S Devices supported R7F701364 
R7F701365 
R7F701362 
R7F701363 
R7F701366 
R7F701367

### Page 3

Renesas Electronics Release Date: 31/10/2016 
 
Page 3 of 56 
As there was no impact on MCAL identified due to the ICU-S unit, Renesas recommends to use the below equivalent 
devices part number without ICU-S unit, during MCAL configuration, instead of the actual device part number with 
ICU-S unit: 
 
Device (with ICU-S Support) Equivalent device(w/o ICU-S support) 
R7F701364 R7F701320 
R7F701365 R7F701321 
R7F701362 R7F701318 
R7F701363 R7F701319 
R7F701366 R7F701322 
R7F701367 R7F701323 
 
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
NA - - 
1.3.3 Additional software 
Tool Version Options 
NA - -

### Page 4

Renesas Electronics Release Date: 31/10/2016 
 
Page 4 of 56 
1.4 Generic Information 
1.4.1 Release Target 
Processor P1M - R7F701310 
Module Generic 
Module Overview User Manual R20UT3752EJ0100-AUTOSAR.pdf – V1.0.9 
Getting Started for P1x MCAL User 
Manual 
R20UT3753EJ0100-AUTOSAR.pdf – V1.0.7 
Date 31-Oct-2016 
1.4.2 Release Items 
Filename Version Change Description 
Generator Files 
P1x_translation.h 1.0.7 No changes for release Ver4.01.01.D 
Common Files 
ComStack_Types.h 1.0.1 No changes for release Ver4.01.01.D 
Std_Types.h 1.0.1 No changes for release Ver4.01.01.D 
rh850_Types.h 1.0.4 No changes for release Ver4.01.01.D 
Platform_Types.h 1.0.1 No changes for release Ver4.01.01.D 
Compiler Files 
Compiler.h 1.0.5 No changes for release Ver4.01.01.D 
Compiler_Cfg.h 1.0.5 No changes for release Ver4.01.01.D 
MemMap.h 1.0.9 Following changes are made in Ver4.01.01.D:- 
1. Removed unwanted memory sections. Also corrected the 
section name of .FLS_CFG_DA TA_UNSPECIFIED for 
FLS module. 
2. Removed unwanted memory sections of MCU module. 
3. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for FLS module. 
4. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for MCU module. 
5. Removed unwanted memory section 
SPI_START_SEC_V AR_BOOLEAN for SPI module. 
6. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for WDG module. 
7. Removed unwanted memory sections of WDG module. 
8. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for SPI module.

### Page 5

Renesas Electronics Release Date: 31/10/2016 
 
Page 5 of 56 
9. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for DIO module. 
10. Removed unwanted memory sections of DIO module. 
11. Removed unwanted memory sections of PORT module. 
12. Memory section _NOINIT_ changed to _NO_INIT_ to 
follow initialization policy of variables for PORT module. 
Os.h 1.0.1 No changes for release Ver4.01.01.D 
Os.c 1.0.2 No changes for release Ver4.01.01.D 
RUCG Tool 
RUCG.exe 1.1 No changes for release Ver4.01.01.D 
Getting Started for P1x MCAL User Manual 
R20UT3752EJ0100-AUTOSAR.pdf 1.0.7 Following changes are made in Ver4.01.01.D:- 
1. Chapter 2 and 3 removed to make the document 
independent of any specific tool. 
2. Autosar version 3.2.2 version check removed from section 
3.2.1. 
Module Overview User Manual 
R20UT3753EJ0100-AUTOSAR.pdf 1.0.9 Following changes are made in Ver4.01.01.D:- 
1. R-Number has been update. 
2. Table 3-12 alignment is corrected. 
RUCG Tool User Manual 
R20UT3754EJ0100-AUTOSAR.pdf 1.1.2 Following change is made in Ver4.01.01.D:- 
1. R-Number corrected for the document 
1.4.3 Known Issues 
ID Description 
NA Please refer to the known issues list as shared from Renesas 
Ref. P1x_AR4.0_KnownIssues_CW43_2016.xlsx.

### Page 6

Renesas Electronics Release Date: 31/10/2016 
 
Page 6 of 56 
1.5 Module Index 
 
DIO 
 
FLS 
 
MCU 
 
PORT 
 
SPI 
 
WDG

### Page 7

Renesas Electronics Release Date: 31/10/2016 
 
Page 7 of 56 
2 DIO 
2.1 Target Info 
Processor P1M - R7F701310 
Module DIO 
Software Version 1.0.11 
Embedded User Manual R20UT3708EJ0100-AUTOSAR.pdf – V1.0.9 
Tool User Manual R20UT3709EJ0100-AUTOSAR.pdf – V1.0.5 
Date 31-Oct-2016 
2.2 Release Items 
Filename Version Change Description 
P1x- Parameter Definition files 
R403_DIO_P1M_04_05_12_13_20_
21.arxml 
1.0.5 Following changes are made in Ver4.01.01.D:- 
1. As per EAAR_PN0034_FSR_0001, the Container 
DioDemEventParameterRefs and Dem error 
DIO_E_REG_WRITE_VERIFY are added. 
2. As per EAAR_PN0034_FSR_0002, the enum parameter 
DioWriteVerify is added. 
3. As per EAAR_PN0034_FSR_0003, the parameter 
DioUseWVErrorInterface is added. 
4. As per EAAR_PN0034_FSR_0004, the callback function is 
introduced in Dio_Cbk.h file. 
5. Corrected warranty disclaimer description. 
R403_DIO_P1M_10_11_14_15_18_
19_22_23.arxml 
1.0.6 Following changes are made in Ver4.01.01.D:- 
1. As per EAAR_PN0034_FSR_0001, the Container 
DioDemEventParameterRefs and Dem error 
DIO_E_REG_WRITE_VERIFY are added. 
2. As per EAAR_PN0034_FSR_0002, the enum parameter 
DioWriteVerify is added. 
3. As per EAAR_PN0034_FSR_0003, the parameter 
DioUseWVErrorInterface is added. 
4. As per EAAR_PN0034_FSR_0004, the callback function is 
introduced in Dio_Cbk.h file. 
5. Corrected warranty disclaimer description. 
BSWMDT 
R403_DIO_P1x_BSWMDT.arxml 1.0.6 Following changes are made in Ver4.01.01.D:- 
1. Software patch version is updated. 
2. Module entries and Exclusive area tags are added for all

### Page 8

Renesas Electronics Release Date: 31/10/2016 
 
Page 8 of 56 
Called entities. 
3. Corrected warranty disclaimer description. 
Source Code 
Dio.c 1.0.23 Following changes are made in Ver4.01.01.D:- 
1. File Dio_Cbk.h is included. 
2. The macro DIO_REG_WRITE and 
DIO_REG_WRITE_VERIFY_RUNTIME are introduced 
in APIs Dio_WritePort, Dio_WriteChannel, 
Dio_FlipChannel,Dio_WriteChannelGroup, 
Dio_MaskedWritePort. 
3. Dio_GetVersionInfo API is added. 
4. Removed MISRA justifications for 4:4397. 
5. Removed dead code. 
6. 'DIO_UT_001' Tag added for the non-covered parts of the 
code. 
7. DET Pre compile check is removed from "LddPortLevel = 
DIO_ZERO" in Dio_ReadPort. 
8. Variable LunPSRContent is initialized as DIO_ZERO in 
Dio_WriteChannel API. 
9. 'DIO_ESDD_UD_XXX' and Req ID Tags are added. 
10. Variable "LddPortModeLevel" is renamed as 
"LulPortModeLevel". 
11. Inclusion of "Dio_Cbk.h" is removed as part of acceptance. 
Dio_Ram.c 1.0.9 Following changes are made in Ver4.01.01.D:- 
1. Removed dead code. 
2. Memory sections SEC_V AR_NOINIT_UNSPECIFIED and 
SEC_V AR_NOINIT_16 changed to 
SEC_V AR_NO_INIT_UNSPECIFIED and 
SEC_

*Excerpt: first 8 of 56 pages shown.*
