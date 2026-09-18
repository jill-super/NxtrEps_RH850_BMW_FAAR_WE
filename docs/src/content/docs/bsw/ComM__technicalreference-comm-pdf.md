---
title: 'ComM — TechnicalReference_ComM'
description: 'Converted PDF document TechnicalReference_ComM.pdf from module ComM.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_ComM.pdf` (PDF, 1059 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 70; title: MICROSAR Communication Manager; author: Michael Schligerski

## Converted content

### Page 1

MICROSAR Communication Manager 
Technical Reference 
 
 
Version 8.00.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Michael Schligerski 
Status Released

### Page 2

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 2 
based on template version 5.2.0 
Document Information 
History 
Author Date Version Remarks 
Michael Schligerski 2012-08-07 1.00.00 Initial creation 
Michael Schligerski 2013-01-31 1.01.00 > Updated AUTOSAR Architecture, chapter 2.1 
> Updated description of 
ComM_CurrentChannelRequest, chapter 6.1.3.1 
Michael Schligerski 2013-05-15 1.02.00 > Added configuration variant Post-Build Loadable, 
chapter 3.1.2.2 (ESCAN00064954) 
> Information from chapter ‘AUTOSAR Standard 
Compliance’ is moved to chapter ‘Features’ 
> Updated chapter ‘Critical Sections’ 
> Removed chapter ‘Compiler Abstraction and 
Memory Mapping’ 
> Updated chapter ‘Partial Network States’ 
Michael Schligerski 2013-09-27 2.00.00 > Updated chapter ‘Partial Network States’ 
(ESCAN00069988) 
> Updated chapters ‘Mode Limitation’, 
‘ComM_PreventWakeUp’, 
‘ComM_LimitChannelToNoComMode’, 
‘ComM_LimitECUToNoComMode’ 
(ESCAN00068896 , ESCAN00068902) 
> Support EthSM as lower layer of COMM, see 
chapters 3.3 and 5.3 (ESCAN00069043) 
> Updated description of Sender Receiver 
Interface ‘ComM_CurrentMode’ 
(ESCAN00070321). 
> Added notes for usage of LIN NM and J1939 NM 
in chapters 3.5.1 and 3.5.3 (ESCAN00071341). 
> Updated Include Structure to reflect Post Build 
Loadable (ESCAN00064954). 
> Added a Caution box to chapter 3.4 regarding 
Partial Network TX EIRA signals 
(ESCAN00071527). 
Michael Schligerski 2014-02-07 2.01.00 > ESCAN00072763 Added DET error 
COMM_E_DIAGNOSTIC_NOT_SUPPORTED in 
chapters 3.6.1, 5.4.4 and 5.4.5 
> ESCAN00074243 Table 3-5 sorted by ID, 
description of the Port Interface 
ComM_CurrentMode moved to chapter 6.1.2 
‘Mode Switch Interface’.

### Page 3

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 3 
based on template version 5.2.0 
Michael Schligerski 2014-06-04 3.00.00 > Improved description of 
ComM_CurrentChannelRequest 
(ESCAN00075361). 
> Improved description of 
ComMPncPrepareSleepTimer in chapter 3.4 
(ESCAN00075422). 
> Added chapter 3.1.3.2 (ESCAN00076076). 
> Adapted chapter 6.1.1.1.3 (ESCAN00074321). 
Michael Schligerski 2014-10-02 3.01.00 > Added support of Bus Type INTERNAL, refer to 
chapter 3.5 (ESCAN00076859) 
> Added Timer-based shutdown synchronization 
via Silent state, refer to chapter 3.1.2.3 and 
Figure 3-1 COMM channel state machine 
(ESCAN00076774) 
> Updated include structure in 4.2 
(ESCAN00078688) 
> Extended Partial Network Cluster ID support, 
refer to chapter 3.1.2 (ESCAN00076852) 
> NvM support made optional, refer to chapter 
3.1.2 (ESCAN000772069) 
> Added internal function service IDs 
(ESCAN00076325) 
Michael Schligerski 2015-03-25 4.00.00 > Support of channel-specific Minimum Full Com 
Mode timer, chapters 3.1.2.4 and 3.3 
(ESCAN00082062) 
Michael Schligerski 2015-08-12 5.00.00 > ‘Post-Build Loadable’ is used as standard 
MICROSAR feature name, chapter 3.1.2.2 
> Service Port names do not contain ComM user 
and channel identifiers anymore, see chapter 6 
(ESCAN00084462) 
> Added Pnc to Channel Routing Limitation, see 
chapter 3.1.2.5 (ESCAN00083603) 
Michael Schligerski 2016-01-12 6.00.00 > Improved description of 3.1.1 Deviations 
(ESCAN00087416) 
Michael Schligerski 2016-02-26 7.00.00 > Added support of Extended RAM Check, see 
chapter 3.1.2.6 (ESCAN00089104) 
> Improved description of 4.3 Critical Sections 
(ESCAN00088182) 
Michael Schligerski 2016-05-24 7.00.01 > Added API description of 
ComM_Nm_StateChangeNotification and 
C

### Page 4

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 4 
based on template version 5.2.0 
Michael Schligerski 2016-08-15 7.01.00 > Added APIs ComM_GetDcmRequestStatus and 
ComM_GetMinFullComModeTimerStatus 
(ESCAN00091481) 
> Provided more details on Nm Variant PASSIVE 
in chapters 3.1.2 and 3.5.1 
Michael Schligerski 2016-11-09 8.00.00 > Added Reset after Forcing NO_COM 
functionality in chapter 3.5.2.1

### Page 5

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 5 
based on template version 5.2.0 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_COMManager.pdf V4.0.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf V3.2.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V1.6.0 
[4] AUTOSAR AUTOSAR_SWS_EthernetStateManager V2.0.0 
[5] AUTOSAR AUTOSAR_SWS_UDPNetworkManagement V3.0.0 
[6] Vector TechnicalReference_LinNm.pdf see delivery 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 6

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 6 
based on template version 5.2.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 11 
2 Introduction ................................ ................................ ................................ .................. 12 
2.1 Architecture Overview ................................ ................................ ............................ 13 
3 Functional Description ................................ ................................ ................................ 15 
3.1 Features ................................ ................................ ................................ ................. 15 
3.1.1 Deviations ................................ ................................ ................................ ..... 16 
3.1.1.1 Variant Post-Build ................................ ................................ ................... 16 
3.1.2 Additions/ Extensions ................................ ................................ .................... 16 
3.1.2.1 Memory Initialization ................................ ................................ ............... 17 
3.1.2.2 Post-Build Loadable ................................ ................................ ............... 17 
3.1.2.3 Timer-based Shutdown Synchronization via Silent State ........................ 17 
3.1.2.4 Channel-specific Minimum Full Com Mode Timer ................................ ... 17 
3.1.2.5 Pnc to Channel Routing Limitation................................ .......................... 18 
3.1.2.6 Extended RAM Check ................................ ................................ ............ 20 
3.1.3 Limi

### Page 7

Technical Reference MICROSAR Communication Manager 
© 2016 Vector Informatik GmbH Version 8.00.00 7 
based on template version 5.2.0 
4.4 Handling of non-volatile Data ................................ ................................ ................. 37 
5 API Description ................................ ................................ ................................ ............ 39 
5.1 Type Definitions ................................ ................................ ................................ ...... 39 
5.2 Services provided by COMM ................................ ................................ .................. 41 
5.2.1 ComM_InitMemory ................................ ................................ ........................ 41 
5.2.2 ComM_Init ................................ ................................ ................................ ..... 41 
5.2.3 ComM_DeInit ................................ ................................ ................................ 42 
5.2.4 ComM_GetStatus ................................ ................................ ...................

*Excerpt: first 8 of 70 pages shown.*
