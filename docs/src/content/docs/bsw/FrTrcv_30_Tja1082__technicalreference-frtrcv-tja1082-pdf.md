---
title: 'FrTrcv_30_Tja1082 — TechnicalReference_FrTrcv_Tja1082'
description: 'Converted PDF document TechnicalReference_FrTrcv_Tja1082.pdf from module FrTrcv_30_Tja1082.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_FrTrcv_Tja1082.pdf` (PDF, 753 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 28; title: MICROSAR FlexRay Transceiver Driver; author: -

## Converted content

### Page 1

MICROSAR FlexRay Transceiver Driver 
Technical Reference 
 
Tja1082 
Version 2.00.00 
 
 
 
 
 
 
 
 
 
 
 
Status Released

### Page 2

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 1 
based on template version 5.7.1 
Document Information 
History 
Date Version Remarks 
2014-05-15 1.00.00 Creation of document 
2015-05-27 1.00.01 ESCAN00078929: Missing explanation of API 
FrTrcv_30_Tja1082_GetVersionInfo 
ESCAN00077241 AR3-2679: Description BCD-coded return-value 
of XXX_GetVersionInfo() in TechRef 
2016-11-04 1.01.00 Support of AUTOSAR 3 
2017-08-25 2.00.00 Rework for SafeBsw 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_FlexRayTransceiverDriver.pdf 1.5.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf 2.2.1 
[3] AUTOSAR AUTOSAR_SWS_DEM.pdf 2.2.0 
[4] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf 1.0.0 
[5] NXP TJA1082.pdf Rev.6 
[6] NXP TJA1083.pdf Rev.1 
 
Scope of the Document 
This technical reference describes the general use of the FlexRay Transceiver Driver basis 
software for Tja1082 or Tja1083 . Please refer to your Release Notes to get a detailed 
description of the platform (Host, CC, Compiler, Transceiver) your Vector FlexRay Bundle 
has been configured for. 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 2 
based on template version 5.7.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 5 
2 Introduction................................ ................................ ................................ ................... 6 
2.1 Supported Devices ................................ ................................ ............................. 7 
2.2 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 8 
3.1 Features ................................ ................................ ................................ ............ 8 
3.1.1 Deviations ................................ ................................ .......................... 8 
3.1.1.1 AUTOSAR 4 ................................ ................................ .... 8 
3.1.2 Limitations ................................ ................................ .......................... 8 
3.1.2.1 Error indication ................................ ................................ . 8 
3.2 Initialization ................................ ................................ ................................ ........ 8 
3.2.1 High-Level Initialization ................................ ................................ ...... 8 
3.2.2 Low-Level Initialization ................................ ................................ ....... 9 
3.3 States ................................ ................................ ................................ ................ 

### Page 4

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 3 
based on template version 5.7.1 
5.2.1.4 FrTrcv_30_Tja1082_GetVersionInfo: Read Version 
Information of the Driver ................................ ................ 16 
5.2.1.5 FrTrcv_30_Tja1082_SetTransceiverMode: Set the 
Transceiver in the requested mode ................................ 17 
5.2.1.6 FrTrcv_30_Tja1082_GetTransceiverMode: Get the 
current Transceiver mode ................................ .............. 18 
5.2.1.7 FrTrcv_30_Tja1082_GetTransceiverWUReason: Get 
the wake up reason................................ ........................ 19 
5.2.1.8 FrTrcv_30_Tja1082_ClearTransceiverWakeup: Clear 
pending wake up events ................................ ................ 20 
5.2.1.9 FrTrcv_30_Tja1082_GetTransceiverError: Read current 
Transceiver error ................................ ............................ 20 
5.2.1.10 FrTrcv_30_Tja1082_DisableTransceiverBranch: Disable 
an individual branch ................................ ....................... 21 
5.2.1.11 FrTrcv_30_Tja1082_EnableTransceiverBranch: Disable 
an individual branch ................................ ....................... 22 
5.3 Services used by FlexRay Transceiver Driver ................................ .................. 23 
5.4 Callback Functions ................................ ................................ ........................... 23 
5.4.1 FrTrcv_30_Tja1082_CheckWakeupByTransceiver ........................... 23 
5.5 Configurable Interfaces ................................ ................................ .................... 24 
5.5.1 Notifications ................................ ................................ ..................... 24 
5.5.1.1 Appl_FrTrcv_30_Tja108

### Page 5

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 4 
based on template version 5.7.1 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 7 
Figure 5-1 Interface Overview FlexRay Transceiver Driver ................................ ........ 13 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 5 
Table 3-1 Service IDs ................................ ................................ ............................... 10 
Table 3-2 Errors reported to DET ................................ ................................ ............. 10 
Table 3-3 Errors reported to DEM ................................ ................................ ............. 10 
Table 4-1 Static files ................................ ................................ ................................ . 11 
Table 4-2 Generated files ................................ ................................ ......................... 11 
Table 5-1 Type definitions ................................ ................................ ......................... 14 
Table 5-2 FrTrcv_30_Tja1082_GenConfigType ................................ ........................ 14 
Table 5-3 FrTrcv_30_Tja1082_ChannelType ................................ ............................ 14 
Table 5-4 FrTrcv_30_Tja1082_InitMemory ................................ ............................... 15 
Table 5-5 FrTrcv_30_Tja1082_Init ................................ ................................ ............ 16 
Table 5-6 FrTrcv_30_Tja1082_MainFunction ................................ ........................... 16 
Table 5-7 FrTrcv_30_Tja1082_GetVersi

### Page 6

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 5 
based on template version 5.7.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 ESCAN00075721 Creation of component 
1.01.00 ESCAN00092491 Support AR3 
2.00.00 STORY-1874 Create Safe BSW Transceiver Driver for Tja1082 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR FlexRay Transceiver Driver 
© 2017 Vector Informatik GmbH Version 2.00.00 6 
based on template version 5.7.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module FlexRay Transceiver Driver as specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: pre-compile 
Vendor ID: FlexRay Transce

*Excerpt: first 8 of 28 pages shown.*
