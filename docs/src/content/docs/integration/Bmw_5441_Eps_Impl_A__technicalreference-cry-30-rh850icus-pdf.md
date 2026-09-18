---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Cry_30_Rh850Icus'
description: 'Converted PDF document TechnicalReference_Cry_30_Rh850Icus.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Cry_30_Rh850Icus.pdf` (PDF, 1157 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 81; title: MICROSAR CRY DRIVER; author: Tobias Finke

## Converted content

### Page 1

MICROSAR CRY DRIVER 
Technical Reference 
 
DrvCry_Rh850Icus 
Version 1.06.01 
 
 
 
 
 
 
 
 
 
 
 
Authors Tobias Finke 
Status Released

### Page 2

Technical Reference MICROSAR CRY DRIVER 
© 2017 Vector Informatik GmbH Version 1.06.01 2 
Based on template version 5.2.0 
Document Information 
History 
Author Date Version Remarks 
Tobias Finke 2015-05-22 1.00.00 Initial Version of MICROSAR CRY DRIVER 
Tobias Finke 2015-07-28 1.01.00 - Added Sym Key Wrapping Service. 
- Added prerequisites for the Initialization. 
- Added Limitation for multiple calls of 
some Cry_<Primitive>Update() functions. 
Tobias Finke 2015-08-20 1.02.00 - Added Limitation: Different Services can’t 
be accessed in parallel. 
- Added description for aborting services. 
- Changed include structure. 
Tobias Finke 2016-01-11 1.02.01 - Cry_ShePrngGenerate accepts a 
resultLength smaller than 16 byte. 
Tobias Finke 2016-06-17 1.03.00 - Config option if length of mac in 
MacVerify is interpreted as bits. 
- Config option how keyIds are mapped. 
- Config option for ICUS base address. 
- Change in the way how M4 and M5 are 
returned after key provisioning. 
Tobias Finke 2016-08-01 1.03.01 - Added Timeout-API 
- Changed default mapping in the mapped 
Use-Case for RAM_KEY from 0xEE to 
0x00. 
Tobias Finke 2016-11-24 1.04.00 - Added Configuration with DaVinci 
Configurator 5 
- Removed 
SymKeyWrapForkeyProvisioning 
Tobias Finke 2017-04-06 1.05.00 - Updated function descriptions 
- Config option for FHVE support 
- Config option for hardware error code 
callout 
- Config option for data flash control 
callouts 
- Config option for data flash 
synchronization callouts. 
- Description of exclusive areas 
Tobias Finke 2017-04-13 1.05.01 - Fixed formatting and spelling 
Tobias Finke 2017-07.14 1.05.02 - Adaption to base component 
Tobias Finke 2017-10-12 1.06.00 - Added Self Test 
- SafeBsw Release 
Tobias Finke 2017-10-19 1.06.01 - Changed include structure

### Page 3

Technical Reference MICROSAR CRY DRIVER 
© 2017 Vector Informatik GmbH Version 1.06.01 3 
Based on template version 5.2.0 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_CryptoServiceManager.pdf 1.2.0 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
[3] HIS SHE - Functional Specification 1.1 
[4] RENESAS User’s Manual: RH850/F1L ICUSB 1.00 
 
 
 
 
 
 
 
 
Caution 
This symbol calls your attention to warnings. 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR CRY DRIVER 
© 2017 Vector Informatik GmbH Version 1.06.01 4 
Based on template version 5.2.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 9 
2 Introduction................................ ................................ ................................ ................. 11 
2.1 Architecture Overview ................................ ................................ ...................... 12 
3 Functional Description ................................ ................................ ............................... 14 
3.1 Features ................................ ................................ ................................ .......... 14 
3.2 Initialization ................................ ................................ ................................ ...... 14 
3.3 States ................................ ................................ ................................ .............. 15 
3.4 Main Functions ................................ ................................ ................................ 16 
3.5 Asynchronous Handling ................................ ................................ ................... 16 
3.6 Key Handling ................................ ................................ ................................ ... 17 
3.7 Key Mapping ................................ ................................ ................................ .... 17 
3.8 Key Update ................................ ................................ ................................ ...... 18 
3.9 General procedure of service execution ................................ ........................... 18 
3.10 Timeout Handling ...............................

### Page 5

Technical Reference MICROSAR CRY DRIVER 
© 2017 Vector Informatik GmbH Version 1.06.01 5 
Based on template version 5.2.0 
5.3.1.5 Cry_30_Rh850Icus_KeyExtractConfigType ................... 32 
5.3.1.6 Cry_30_Rh850Icus_KeyWrapSymConfigType ............... 33 
5.3.1.7 Cry_30_Rh850Icus_RngConfigType .............................. 33 
5.4 Services provided by CRY_30_RH850ICUS ................................ .................... 34 
5.4.1 Cry_30_Rh850Icus_Init ................................ ................................ .... 34 
5.4.2 Cry_30_Rh850Icus_InitMemory ................................ ....................... 34 
5.4.3 Cry_30_Rh850Icus_GetVersionInfo ................................ ................. 35 
5.4.4 Cry_30_Rh850Icus_AesEncrypt128Start ................................ ......... 36 
5.4.5 Cry_30_Rh850Icus_AesEncrypt128Update ................................ ..... 37 
5.4.6 Cry_30_Rh850Icus_AesEncrypt128Finish ................................ ....... 39 
5.4.7 Cry_30_Rh850Icus_AesEncrypt128MainFunction ........................... 40 
5.4.8 Cry_30_Rh850Icus_AesDecrypt128Start ................................ ......... 41 
5.4.9 Cry_30_Rh850Icus_AesDecrypt128Update ................................ ..... 42 
5.4.10 Cry_30_Rh850Icus_AesDecrypt128Finish ................................ ....... 44 
5.4.11 Cry_30_Rh850Icus_AesDecrypt128MainFunction ........................... 45 
5.4.12 Cry_30_Rh850Icus_CmacAes128GenStart ................................ ..... 46 
5.4.13 Cry_30_Rh850Icus_CmacAes128GenUpdate ................................ . 47 
5.4.14 Cry_30_Rh850Icus_CmacAes128GenFinish ................................ ... 48 
5.4.15 Cry_30_Rh850Icus_CmacAes128GenMainFunction ....................... 50 
5.4.16 Cry_30_Rh850Icus_CmacAes128VerStart ...........

### Page 6

Technical Reference MICROSAR CRY DRIVER 
© 2017 Vector Informatik GmbH Version 1.06.01 6 
Based on template version 5.2.0 
5.5.1.2 Timeout-API Loop Callout ................................ .............. 73 
5.5.1.3 Cry_30_Rh850Icus_HardwareErrorCode_Callout .......... 73 
5.5.1.4 Cry_30_Rh850Icus_DataFlashReadStart_Callout ......... 74 
5.5.1.5 Cry_30_Rh850Icus_DataFlashReadEnd_Callout .......... 74 
5.5.1.6 Cry_30_Rh850Icus_DataFlashWriteStart_Callout .......... 75 
5.5.1.7 Cry_30_Rh850Icus_DataFlashWriteEnd_Callout ........... 75 
5.5.1.8 Cry_30_Rh850Icus_DataFlashSetReadMode_Callout ... 76 
5.5.1.9
Cry_30_Rh850Icus_DataFlashReturnFromCommandLockedState_Callout 76 
5.6 Services used by CRY_30_RH850ICUS ................................ .......................... 77 
5.7 Service Ports ................................ ................................ ................................ ... 77 
6 Configuration ................................ ................................ ................................ .............. 78 
6.1 Configuration Variants ................................ ................................ ...................... 78 
6.2 Deviations ................................ ................................ ................................ ........ 78 
6.3 Additions/ Extensions ................................ ................................ ....................... 78 
6.3.1 Timeout handling ................................ ................................ .............. 78 
6.3.2 Hardware error callout ................................ ..............

*Excerpt: first 8 of 81 pages shown.*
