---
title: 'FrSM — TechnicalReference_FrSM'
description: 'Converted PDF document TechnicalReference_FrSM.pdf from module FrSM.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_FrSM.pdf` (PDF, 1023 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 32; title: YourTopic; author: Mark A. Fingerle

## Converted content

### Page 1

MICROSAR FlexRay State Manager 
Technical Reference 
 
 
Version 1.2.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Mark A. Fingerle 
Status Released

### Page 2

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 2 
based on template version 4.9.2 
Document Information 
History 
Author Date Version Remarks 
Mark A. Fingerle 2012-08-08 1.0.0 Creation from scratch 
Mark A. Fingerle 2014-10-13 1.1.0 ESCAN00076761 Post-Build Selectable 
(Identity Manager) support 6.1.3 
ESCAN00075457 Add support for delayed 
FlexRay communication cluster shutdown 
3.3.8, 6.2.5 
ESCAN00079339 Description BCD-coded 
return-value of GetVersionInfo() 
Mark A. Fingerle 2016-05-13 1.2.0 Add missing API 5.2.8 
FrSM_SetEcuPassive 
FEAT-2724 Handle several FlexRay 
clusters Table 3-1 Supported AUTOSAR 
standard conform features, Table 3-2 Not 
supported AUTOSAR standard conform 
features 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR Specification of FlexRay State Manager 2.2.0 
[2] AUTOSAR Specification of Development Error Tracer 3.2.0 
[3] AUTOSAR Specification of Diagnostics Event Manager 4.2.0 
[4] AUTOSAR List of Basic Software Modules 1.6.0 
[5] AUTOSAR Specification of FlexRay Interface 3.3.0 
[6] AUTOSAR Specification of Communication Manager 4.0.0 
[7] AUTOSAR Specification of Basic Software Mode Manager 1.2.0 
Scope of the Document 
This technical reference describes the general use of the FlexRay State Manager basis 
software. All aspects which are FlexRay controller specific are described in the technical 
reference of the FlexRay Interface, which is also part of the delivery. 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector’s release of the programs delivered to your 
company is expressly restricted to the configuration you 

### Page 3

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 3 
based on template version 4.9.2 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 Features ................................ ................................ ................................ ............ 9 
3.2 Initialization ................................ ................................ ................................ ...... 10 
3.3 State Machine ................................ ................................ ................................ .. 11 
3.3.1 Meta States FullCom / NoCom ................................ ......................... 12 
3.3.2 FRSM_INITIAL ................................ ................................ ................. 12 
3.3.3 FRSM_STARTUP / FRSM_WAKEUP / FRSM_READY ................... 12 
3.3.4 FRSM_WAKEUP , Send Multiple Wake-Up Pattern ........................... 13 
3.3.5 FRSM_STATE_ONLINE ................................ ................................ ... 13 
3.3.6 FRSM_KEY_SLOT_ONLY ................................ ............................... 14 
3.3.7 FRSM_STATE_ONLINE_PASSIVE ................................ .................. 14 
3.3.8 FRSM_STATE_HALT_REQ ................................ ............................. 14 
3.3.9 Startup Monitoring (FRSM_STA

### Page 4

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 4 
based on template version 4.9.2 
5.2.3 FrSM_MainFunction_<Cluster Id> ................................ .................... 24 
5.2.4 FrSM_RequestComMode................................ ................................ . 24 
5.2.5 FrSM_GetCurrentComMode ................................ ............................ 25 
5.2.6 FrSM_GetVersionInfo ................................ ................................ ....... 25 
5.2.7 FrSM_AllSlots ................................ ................................ .................. 26 
5.2.8 FrSM_SetEcuPassive ................................ ................................ ...... 26 
5.3 Services Used by FrSM ................................ ................................ ................... 27 
6 AUTOSAR Standard Compliance................................ ................................ ............... 29 
6.1 Additions/ Extensions ................................ ................................ ....................... 29 
6.1.1 API FrSM_InitMemory() ................................ ................................ ... 29 
6.1.2 Configuration Options ................................ ................................ ...... 29 
6.1.3 Post-Build Selectable (Identity Manager) ................................ ......... 29 
6.2 Limitations................................ ................................ ................................ ........ 29 
6.2.1 Controllers ................................ ................................ ....................... 29 
6.2.2 Shy of Coldstarter ................................ ................................ ............ 29 
6.2.3 Configuration Class ................................ ........

### Page 5

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 5 
based on template version 4.9.2 
Illustrations 
Figure 2-1 AUTOSAR architecture ................................ ................................ ............... 7 
Figure 2-2 Interfaces to adjacent modules of the FrSM ................................ ................ 8 
Figure 3-1 State machine of the FrSM ................................ ................................ ....... 11 
Figure 4-1 Include structure ................................ ................................ ....................... 19 
 
Tables 
Table 1-1 Component History ................................ ................................ ..................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 9 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 9 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 10 
Table 3-4 Service IDs ................................ ................................ ............................... 16 
Table 3-5 Errors reported to Det ................................ ................................ ............... 16 
Table 3-6 Errors reported to Dem ................................ ................................ ............. 17 
Table 4-1 Static files ................................ ................................ ................................ . 18 
Table 4-2 Generated files ................................ ................................ ......................... 18 
Table 4-3 Compiler abstraction and memory mapping ................................ .............. 20 
Table 5-1 Type definitions ................................ 

### Page 6

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 6 
based on template version 4.9.2 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.0.0 Creation according to AUTOSAR 4.0.3 
Table 1-1 Component History

### Page 7

Technical Reference MICROSAR FlexRay State Manager 
© 2017 Vector Informatik GmbH Version 1.2.0 7 
based on template version 4.9.2 
2 Introduction 
This document describes the fun

*Excerpt: first 8 of 32 pages shown.*
