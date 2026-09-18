---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Cdd_Communication'
description: 'Converted PDF document TechnicalReference_Cdd_Communication.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Cdd_Communication.pdf` (PDF, 667 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 45; title: MICROSAR Complex Device Driver; author: Safiulla Shakir, Gunnar Meiss, Markus Bart

## Converted content

### Page 1

MICROSAR Complex Device Driver 
Technical Reference 
 
DaVinci Configurator 
Version 2.04.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Safiulla Shakir, Gunnar Meiss, Markus Bart 
Status Released

### Page 2

Technical Reference MICROSAR Complex Device Driver 
© 2017 Vector Informatik GmbH Version 2.04.00 2 
based on template version 5.2.0 
Document Information 
History 
Author Date Version Remarks 
Safiulla Shakir 2012-03-23 1.00.00 Initial Version 
Gunnar Meiss 2012-08-08 2.00.00 Support AUTOSAR 4 
Gunnar Meiss 2013-05-13 2.00.01 performed review rework 
Markus Bart 2014-02-05 2.01.00 Support J1939Rm Contribution 
Markus Bart 2014-02-28 2.02.00 Support the StartOfReception API with the 
PduInfoType according to ASR4.1.2 
Gunnar Meiss 2014-05-07 2.02.00 AR4-769: ESCAN00075414 
AR4-744: Cdd shall support 
CddSoAdUpperLayerContribution as an 
extension to AR 4.0.3 (schema shall 
remain at AR 4.0.3) 
Gunnar Meiss 2016-02-24 2.03.00 FEAT-1631: Trigger Transmit API with 
SduLength In/Out according to ASR4.2.2 
Gunnar Meiss 2017-01-09 2.04.00 Rename TechnicalReference_Cdd.pdf to 
TechnicalReference_Cdd_Communication.
pdf 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_TPS_ECUConfiguration.pdf 3.2.0 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR Complex Device Driver 
© 2017 Vector Informatik GmbH Version 2.04.00 3 
based on template version 5.2.0 
 
 
Caution 
This symbol calls your attention to warnings. 
 
 
 
Contents 
1 Component History ................................ ................................ ................................ ...... 7 
2 Introduction................................ ................................ ................................ ................... 8 
2.1 Architecture Overview ................................ ................................ ........................ 9 
3 Functional Description ................................ ................................ ............................... 10 
3.1 Features ................................ ................................ ................................ .......... 10 
4 Integration ................................ ................................ ................................ ................... 11 
4.1 Scope of Delivery ................................ ................................ ............................. 11 
4.1.1 Static Files ................................ ................................ ....................... 11 
4.1.2 Dynamic Files ................................ ................................ .................. 11 
4.2 Compiler Abstraction and Memory Mapping ................................ ..................... 11 
5 API Description CddPduRUpperLayerContribution as IF ................................ ........ 12 
5.1 Services used by <CDD> ................................ ................................ ................. 12 
5.2 Callback Functions ................................ ................................ ........................... 12 
5.2.1 <CDD>_RxIndication ......

### Page 4

Technical Reference MICROSAR Complex Device Driver 
© 2017 Vector Informatik GmbH Version 2.04.00 4 
based on template version 5.2.0 
7.1.2 <CDD>_CancelTransmit ................................ ................................ .. 21 
7.2 Services used by <CDD> ................................ ................................ ................. 21 
8 API Description CddPduRLowerLayerContribution as TP ................................ ...... 22 
8.1 Services provided by <CDD> ................................ ................................ ........... 22 
8.1.1 <CDD>_Transmit ................................ ................................ ............. 22 
8.1.2 <CDD>_CancelTransmit ................................ ................................ .. 23 
8.1.3 <CDD>_CancelReceive ................................ ................................ ... 24 
8.1.4 <CDD>_ChangeParameter ................................ .............................. 25 
8.2 Services used by <CDD> ................................ ................................ ................. 25 
9 API Description CddComIfUpperLayerContribution ................................ ................ 26 
9.1 Services used by <CDD> ................................ ................................ ................. 26 
9.2 Callback Functions ................................ ................................ ........................... 26 
9.2.1 <CDD>_RxIndication ................................ ................................ ....... 27 
9.2.2 <CDD>_TxConfirmation ................................ ................................ ... 27 
9.2.3 <CDD>_TriggerTransmit ................................ ................................ .. 28 
10 API Description CddJ1939RmContribution ................................ .....

### Page 5

Technical Reference MICROSAR Complex Device Driver 
© 2017 Vector Informatik GmbH Version 2.04.00 5 
based on template version 5.2.0 
13.1 Deviations ................................ ................................ ................................ ........ 42 
13.2 Additions/ Extensions ................................ ................................ ....................... 42 
13.3 Limitations................................ ................................ ................................ ........ 42 
14 Glossary and Abbreviations ................................ ................................ ...................... 43 
14.1 Glossary ................................ ................................ ................................ .......... 43 
14.2 Abbreviations ................................ ................................ ................................ ... 44 
15 Contact ................................ ................................ ................................ ........................ 45

### Page 6

Technical Reference MICROSAR Complex Device Driver 
© 2017 Vector Informatik GmbH Version 2.04.00 6 
based on template version 5.2.0 
Illustrations 
Figure 2-1 AUTOSAR 4.1 Architecture Overview ................................ ......................... 9 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 7 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 10 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 10 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 10 
Table 4-1 Generated files ................................ ................................ ......................... 11 
Table 5-1 Services used by the <CDD> ................................ ................................ .... 12 
Table 5-2 <CDD>_RxIndication ................................ ................................ ................ 12 
Table 5-3 <CDD>_TxConfirmation ................................ ................................ ........... 13 
Table 5-4 <CDD>_TriggerTransmit ................................ ................................ ........... 14 
Table 6-1 Services used by the <CDD> ................................ ................................ .... 15 
Table 6-2 <CDD>_StartOfReception ................................ ................................ ........ 16 
Table 6-3 <CDD>_CopyRxData ................................ ................................ ............... 16 
Table 6-4 <CDD>_TpRxIndication ................................ ........................

*Excerpt: first 8 of 45 pages shown.*
