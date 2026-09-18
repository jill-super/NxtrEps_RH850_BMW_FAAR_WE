---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_FrIf'
description: 'Converted PDF document TechnicalReference_FrIf.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_FrIf.pdf` (PDF, 1355 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 81; title: MICROSAR FlexRay Interface; author: Oliver Reineke, Anthony Thomas

## Converted content

### Page 1

MICROSAR FlexRay Interface 
Technical Reference 
 
Version 4.01.00 
 
 
 
 
 
 
 
Authors Oliver Reineke, Anthony Thomas 
Status Released

### Page 2

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 2 
based on template version 4.11.3 
Document Information 
History 
Author Date Version Remarks 
Anthony Thomas 2016-04-24 4.00.00 First SafeBSW release. 
Anthony Thomas 2016-07-13 4.00.01 Added deviation related to the job list 
resynchronization. 
Anthony thomas 2017-03-24 4.01.00 Support 2 FlexRay Clusters 
 
Reference Documents 
No. Title Version 
[1] AUTOSAR_FlexRayInterface.pdf V3.2.0 
[2] AUTOSAR_SWS_DET.pdf V2.2.0 
[3] AUTOSAR_SWS_DEM.pdf V2.2.1 
[4] AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[5] TechnicalReference_Asr_Fr.pdf V1.14 or 
later 
[6] TechnicalReference_Asr_FrTrcv_Tja1080.pdf V.1.08 or 
later 
[7] TechnicalReference_Asr_FrNm.pdf V1.3.0 or 
later 
[8] TechnicalReference_Asr_EcuM.pdf V2.1.0 or 
later 
[9] TechnicalReference_Asr_Com.pdf V2.6.0 or 
later 
[10] TechnicalReference_Asr_PduR.pdf V3.4.0 or 
later 
[11] TechnicalReference_Asr_SchM.pdf V2.3.0 or 
later 
[12] AN-ISC-8-1118_MICROSAR_BSW_Compatibility_Check.pdf V1.0 
[13] TechnicalReference_IdentityManager.pdf V1.1.7 or 
later

### Page 3

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 3 
based on template version 4.11.3 
Scope of the Document 
This technical reference describes the general use of the FlexRay Interface basic software. 
 
 
Please note 
We have configured the programs in accordance with your specifications in the questionnaire. 
Whereas the programs do support other configurations than the one specified in your 
questionnaire, Vector´s release of the programs delivered to your company is expressly 
restricted to the configuration you have specified in the questionnaire.

### Page 4

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 4 
based on template version 4.11.3 
Contents 
1 Component History ................................ ................................ ................................ ......... 11 
2 Introduction ................................ ................................ ................................ ...................... 12 
2.1 Architecture Overview ................................................................................................. 13 
3 Functional Description ................................ ................................ ................................ ... 15 
3.1 Features ......................................................................................................................... 15 
3.1.1 Deviations .................................................................................................... 16 
3.1.2 Additions/ Extensions ................................................................................ 17 
3.2 Initialization .................................................................................................................... 17 
3.2.1 Configuration Variants 1 and 2 (Pre-Compile and Link-Time 
Configuration) ............................................................................................. 17 
3.2.2 Configuration Variant 3 (Post-build Configuration) ............................... 18 
3.3 States ............................................................................................................................. 18 
3.4 Main Functions ............................................................................................................. 18 
3.4.1 Cyclic function ............................................

### Page 5

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 5 
based on template version 4.11.3 
3.9 Buffer Reconfiguration ................................................................................................. 29 
3.10 L-PDU Reconfiguration ............................................................................................... 29 
3.11 Dual Channel Redundancy Support .......................................................................... 30 
3.12 Dynamic Payload ......................................................................................................... 32 
4 Integration ................................ ................................ ................................ ........................ 33 
4.1 Scope of Delivery ......................................................................................................... 33 
4.1.1 Static Files ................................................................................................... 33 
4.1.2 Dynamic Files ............................................................................................. 33 
4.2 Include Structure .......................................................................................................... 34 
4.3 Compiler Abstraction and Memory Mapping ............................................................ 35 
4.4 Critical Sections and Exclusive Areas ....................................................................... 35 
4.4.1 FRIF_EXCLUSIVE_AREA_0 ................................................................... 35 
4.4.2 FRIF_EXCLUSIVE_AREA_1 ................................................................... 36 
4.4.3 FRIF_EXCLUSIVE_AREA_2 ...............................................................

### Page 6

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 6 
based on template version 4.11.3 
5.2.11 FrIf_ControllerInit ........................................................................................ 43 
5.2.12 FrIf_DisableLPdu (optional) ...................................................................... 44 
5.2.13 FrIf_DisableAbsoluteTimerIRQ ................................................................ 45 
5.2.14 FrIf_DisableRelativeTimerIRQ ................................................................. 46 
5.2.15 FrIf_DisableTransceiverBranch................................................................ 46 
5.2.16 FrIf_EnableAbsoluteTimerIRQ ................................................................. 47 
5.2.17 FrIf_EnableRelativeTimerIRQ .................................................................. 47 
5.2.18 FrIf_EnableTransceiverBranch ................................................................ 47 
5.2.19 FrIf_GetAbsoluteTimerIRQStatus ............................................................ 48 
5.2.20 FrIf_GetChannelStatus (optional) ............................................................ 49 
5.2.21 FrIf_GetClockCorrection (optional) .......................................................... 50 
5.2.22 FrIf_GetCycleLength .................................................................................. 51 
5.2.23 FrIf_GetGlobalTime ................................................................................... 51 
5.2.24 FrIf_GetMacrotickDuration ........................................................................ 52 
5.2.25 FrIf_GetMacroticksPerCycle ..................................................................... 53 
5.2.26 FrIf_GetNmVector ........................

### Page 7

Technical Reference MICROSAR FlexRay Interface 
© 2017 Vector Informatik GmbH Version 4.01.00 7 
based on template version 4.11.3 
5.2.38 FrIf_InitMemory........................................................................................... 62 
5.2.39 FrIf_JobListExec_<ClstIdx> ...................................................................... 63 
5.2.40 FrIf_MainFunction_<ClstIdx> ................................................................... 63 
5.2.41 FrIf_ReadCCConfig (optional) .................................................................. 64 
5.2.42 FrIf_ReconfigLPdu (optional) ..................................................

*Excerpt: first 8 of 81 pages shown.*
