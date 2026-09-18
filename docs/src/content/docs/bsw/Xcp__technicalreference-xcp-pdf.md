---
title: 'Xcp — TechnicalReference_XCP'
description: 'Converted PDF document TechnicalReference_XCP.pdf from module Xcp.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_XCP.pdf` (PDF, 1081 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 71; title: MICROSAR XCPMICROSAR XCP; author: Andreas HerkommerAndreas Herkommer

## Converted content

### Page 1

MICROSAR XCP 
Technical Reference 
 
 
Version 2.0.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Andreas Herkommer 
Status Released

### Page 2

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Informatik GmbH Version 2.0.02.0.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Andreas Herkommer 2017-02-13 1.00.00 Initial Version 
Andreas Herkommer 2017-11-14 2.00.00 Added new API Xcp_SetStimMode 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_XCP.pdf 2.3.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf 3.4.1 
[3] AUTOSAR AUTOSAR_SWS_DEM.pdf 5.2.0 
[4] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[5] ASAM ASAM_XCP_Part2-Protocol-Layer-Specification_V1-1-
0.pdf 
V1.1 
Scope of the Document 
This document describes the features, APIs, and integration of the XCP Protocol Layer. 
This document does not cover the XCP Transport Layers for CAN, FlexRay and Ethernet, 
which are available at Vector Informatik. 
Further information about XCP on CAN, FlexRay and Ethernet Transport Layers can be 
found in their documentation. 
Please also refer to “The Universal Measurement and Calibration Protocol Family” 
specification by ASAM e.V. 
The XCP Protocol Layer is a hardware independent protocol that can be ported to almost 
any hardware. Due to there are numerous combinations of micro controllers, compilers 
and memory models it cannot be guaranteed that it will run properly on any of the above 
mentioned combinations. 
Please note that in this document the term Application is not used strictly for the user 
software but also for any higher software layer, like e.g. a Communication Control Layer. 
Therefore, Application refers to any of the software components using XCP. 
The API of the functions is described in a separate chapter at the end of this document. 
 
 
Info 
The source code of the XCP Protocol Layer, configuration examples and

### Page 3

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Informatik GmbH Version 2.0.02.0.0 3 
based on template version 6.0.1 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Informatik GmbH Version 2.0.02.0.0 4 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ .... 10 
2 Introduction................................ ................................ ................................ ................. 11 
2.1 Architecture Overview ................................ ................................ ...................... 11 
3 Functional Description ................................ ................................ ............................... 13 
3.1 Features ................................ ................................ ................................ .......... 13 
3.1.1 Deviations ................................ ................................ ........................ 13 
3.1.2 Additions/ Extensions ................................ ................................ ....... 15 
3.2 Initialization ................................ ................................ ................................ ...... 15 
3.3 States ................................ ................................ ................................ .............. 15 
3.4 Main Functions ................................ ................................ ................................ 16 
3.5 Block Transfer Communication Model ................................ .............................. 16 
3.6 Slave Device Identification ................................ ................................ ............... 17 
3.6.1 XCP Station Identifier ................................ ................................ ....... 17 
3.6.2 XCP Generic Identification ................................ ........

### Page 5

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Informatik GmbH Version 2.0.02.0.0 5 
based on template version 6.0.1 
3.14.3 Calibration Data Page Copying ................................ ........................ 24 
3.14.4 Freeze Mode Handling ................................ ................................ ..... 24 
3.15 Flash Programming ................................ ................................ .......................... 25 
3.15.1 Flash Programming by the ECU’s Application ................................ .. 25 
3.15.2 Flash Programming Plug & Play Mechanism ................................ ... 25 
3.15.3 Flash Programming with a Flash Kernel ................................ ........... 26 
3.16 Multi Core Support ................................ ................................ ........................... 26 
3.16.1 Type Safe Copy ................................ ................................ ............... 26 
3.16.2 DAQ/STIM with Multi Core ................................ ............................... 27 
3.17 En- / Disabling the XCP module ................................ ................................ ....... 28 
3.18 XCP measurement during the post event time ................................ ................. 28 
3.19 Error Handling ................................ ................................ ................................ .. 29 
3.19.1 Development Error Reporting ................................ ........................... 29 
3.19.2 Production Code Error Reporting ................................ ..................... 30 
4 Integration ................................ ................................ ................................ ................... 31 
4.1 Scope of Delivery ........................

### Page 6

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Informatik GmbH Version 2.0.02.0.0 6 
based on template version 6.0.1 
5.2.12 Xcp_ModifyProtectionStatus ................................ ............................ 41 
5.2.13 Xcp_GetSessionStatus ................................ ................................ .... 42 
5.2.14 Xcp_GetXcpDataPointer ................................ ................................ .. 42 
5.2.15 Xcp_SetStimMode ................................ ................................ ........... 43 
5.3 Services provided by the XCP Protocol Layer and called by the XCP 
Transport Layer ................................ ................................ ................................ 43 
5.3.1 Xcp_TlRxIndication ................................ ................................ .......... 43 
5.3.2 Xcp_TlTxConfirmation ................................ ................................ ...... 44 
5.3.3 Xcp_SetActiveTl ................................ ................................ ............... 44 
5.3.4 Xcp_GetActiveTl ................................ ................................ .............. 45 
5.4 XCP Transport Layer Services called by the XCP Protocol Layer .................... 46 
5.4.1 <Bus>Xcp_Send ................................ ................................ .............. 46 
5.4.2 <Bus>Xcp_SendFlush ................................ ................................ ..... 47 
5.4.3 <Bus>Xcp_TlService ................................ ................................ ........ 47 
5.5 Application Services called by the XCP Protocol Layer ................................ .... 48 
5.5.1 XcpAppl_GetTimestamp ................................ ................................ .. 49 
5.5.2 XcpAppl_GetPointer

### Page 7

Technical ReferenceTechnical Reference MICROSAR XCPMICROSAR XCP 
© 2017 Vector Info

*Excerpt: first 8 of 71 pages shown.*
