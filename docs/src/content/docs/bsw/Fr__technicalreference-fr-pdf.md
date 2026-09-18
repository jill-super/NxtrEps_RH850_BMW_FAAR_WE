---
title: 'Fr — TechnicalReference_Fr'
description: 'Converted PDF document TechnicalReference_Fr.pdf from module Fr.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Fr.pdf` (PDF, 971 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 57; title: MICROSAR FR; author: Roland Hocke, Matthias Müller

## Converted content

### Page 1

MICROSAR FR 
Technical Reference 
 
Base Content 
Version 1.04.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Roland Hocke, Matthias Müller 
Status Released

### Page 2

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 2 
based on template version 6.0.1 
1 Document Information 
1.1 History 
 
Author Date Version Remarks 
Matthias Müller 2012-11-15 1.0 Initial Version of Autosar 4 
Matthias Müller 2013-07-18 1.0.1 ESCAN00069139: 
Added new restriction to 
section 3.14 FIFO reception 
Matthias Müller 2013-08-01 1.1 ESCAN00067407 
Remove obsolete MTS APIs 
Roland Hocke 2013-10-24 1.2 Added Limitations and the 
description of 
StringentLength- and 
StringentCheck 
Matthias Müller 2014-11-05 1.3 Added feature MICROSAR 
Identity Manager using Post-
Build Selectable 
Matthias Müller 2017-07-05 1.4 Adapted Features and added 
description of 
ApplFr_ISR_Timer0_1 and 
ApplFr_ISR_CycleStart_1. 
 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_FlexRayDriver.pdf 4.3.0 
[2] AUTOSAR_SWS_FlexRayDriver.pdf 2.3.0 
[3] AUTOSAR_SRS_FlexRay.pdf 3.1.0 
[4] AUTOSAR_SRS_FlexRay.pdf 4.3.0 
[5] AUTOSAR_SWS_DET.pdf 2.2.0 
[6] AUTOSAR_SWS_DEM.pdf 2.2.1 
[7] AUTOSAR_BasicSoftwareModules.pdf 1.2.0 
[8] TechnicalReference_ASR_Fr_<CCName>_<platform>.pdf 1.10 or 
later 
[9] FlexRay Communications System Protocol Specification 2.1A 
[10] TechnicalReference_ASR_FrIf.pdf 3.0.7 or 
later 
[11] TechnicalReference_Asr_EcuM.pdf 2.1.0 or 
later

### Page 3

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 3 
based on template version 6.0.1 
[12] TechnicalReference_Asr_FrTp.pdf 1.14.0 or 
later 
[13] TechnicalReference_Asr_AMDRunTimeMeasurement.pdf V1.0 or 
later 
[14] AN-ISC-8-1118 MICROSAR BSW Compatibility Check 1.0 
[15] AUTOSAR_InterruptHandling_Explanation.pdf 1.0.0 or 
later 
[16] http://www.autosar.org/bugzilla/ n/a 
Table 1-2 Reference documents 
 
1.3 Scope of the Document 
This technical reference describes the general use of the FlexRay driver basis software. All 
aspects which are Communication controller specific are described in a separate 
document [8], which is also part of the delivery. 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 4 
based on template version 6.0.1 
Contents 
1 Document Information ................................ ................................ ................................ . 2 
1.1 History ................................ ................................ ................................ ............... 2 
1.2 Reference Documents ................................ ................................ ....................... 2 
1.3 Scope of the Document................................ ................................ ...................... 3 
2 Introduction................................ ................................ ................................ ................... 9 
2.1 Architecture Overview ................................ ................................ ........................ 9 
3 Functional Description ................................ ................................ ............................... 12 
3.1 Features ................................ ................................ ................................ .......... 12 
3.2 Initialization ................................ ................................ ................................ ...... 13 
3.3 Configuration Variants ................................ ................................ ...................... 14 
3.4 States ................................ ................................ ................................ .............. 14 
3.5 Dual bus network usage................................ ................................ ................... 14 
3.6 Main Functions ................................ ................................ ................................ 16 
3.7 Error Handling ................................ ......

### Page 5

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 5 
based on template version 6.0.1 
5.2 Interrupt Service Routines provided by FR ................................ ....................... 28 
5.3 Services provided by FR ................................ ................................ .................. 29 
5.3.1 Fr_InitMemory ................................ ................................ .................. 29 
5.3.2 Fr_Init ................................ ................................ .............................. 29 
5.3.3 Fr_ControllerInit ................................ ................................ ............... 30 
5.3.4 Fr_AllSlots ................................ ................................ ....................... 30 
5.3.5 Fr_StartCommunication ................................ ................................ ... 31 
5.3.6 Fr_HaltCommunication ................................ ................................ .... 31 
5.3.7 Fr_AbortCommunication ................................ ................................ .. 32 
5.3.8 Fr_AllowColdstart ................................ ................................ ............. 32 
5.3.9 Fr_SendWUP ................................ ................................ ................... 33 
5.3.10 Fr_SetWakeupChannel ................................ ................................ .... 33 
5.3.11 Fr_GetPOCStatus ................................ ................................ ............ 34 
5.3.12 Fr_TransmitTxLPdu ................................ ................................ ......... 35 
5.3.13 Fr_ReceiveRxLPdu ................................ ................................ .......... 36 
5.3.14 Fr_CancelTxLPdu ................................ .....................

### Page 6

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 6 
based on template version 6.0.1 
5.6 Configurable Interfaces ................................ ................................ .................... 53 
5.6.1 Notifications ................................ ................................ ..................... 53 
5.6.2 Callout Functions ................................ ................................ ............. 53 
5.6.2.1 ApplFr_ISR_Timer0 ................................ ....................... 53 
5.6.2.2 ApplFr_ISR_Timer0_1 ................................ ................... 54 
5.6.2.3 ApplFr_ISR_CycleStart ................................ .................. 54 
5.6.2.4 ApplFr_ISR_CycleStart_1 ................................ .............. 55 
6 Glossary and Abbreviations ................................ ................................ ...................... 56 
6.1 Glossary ................................ ................................ ................................ .......... 56 
6.2 Abbreviations ................................ ................................ ................................ ... 56 
7 Contact ................................ ................................ ................................ ........................ 57

### Page 7

Technical Reference MICROSAR FR 
© 2017 Vector Informatik GmbH Version 1.04.00 7 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR architecture ................................ ................................ ............. 10 
Figure 2-2 Interfaces to adjacent modules of the Fr ................................ ................... 11 
Figure 3-1 FlexRay Driver Sequence Diagram ................................ ........................... 15 
Figure 4-1

*Excerpt: first 8 of 57 pages shown.*
