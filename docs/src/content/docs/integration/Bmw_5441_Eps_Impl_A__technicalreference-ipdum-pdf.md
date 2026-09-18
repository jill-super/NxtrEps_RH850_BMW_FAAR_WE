---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_IpduM'
description: 'Converted PDF document TechnicalReference_IpduM.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_IpduM.pdf` (PDF, 742 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 25; title: YourTopic; author: Safiulla Shakir, Markus Bart, Gunnar Meiss

## Converted content

### Page 1

MICROSAR I-PDU Multiplexer 
Technical Reference 
 
 
Version 2.06.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Safiulla Shakir, Markus Bart, Gunnar Meiss 
Status Released

### Page 2

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 2 
based on template version 5.2.0 
Document Information 
History 
Author Date Version Remarks 
Safiulla Shakir 2011-12-06 1.00.00 Initial CFG5 version derived from 
TechnicalReference_ASR_IpduM.pdf 
Markus Bart 2012-08-23 2.00.00 ESCAN00058313 
AR4-160: Support AUTOSAR 4.0.3 
Markus Bart 2013-01-29 2.01.00 ESCAN00063294 
AR4-197: Support BIG_ENDIAN Copy 
Segments in IpduM 
Gunnar Meiss 2013-04-04 2.02.00 ESCAN00064368 
AR4-325: Post-Build Loadable 
Markus Bart 2014-11-05 2.03.00 AR4-698: Post-Build Selectable (Identity 
Manager) 
Markus Bart 2014-12-01 2.04.00 FEAT-229: Support 16bit selector in IpduM 
[AR4-927] 
Markus Bart 2015-08-11 2.05.00 FEAT-1315: IPDUM for CAN-FD 
supporting nPdu2Frame-Mapping 
Gunnar Meiss 2016-02-25 2.06.00 FEAT-1631: Trigger Transmit API with 
SduLength In/Out according to ASR4.2.2 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_IPDUMultiplexer.pdf 2.2.0 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
[3] Vector TechnicalReference_PostBuildLoadable.pdf 1.0.0 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire. 
 
 
 
Caution 
This symbol calls your attention to warnings.

### Page 3

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 3 
based on template version 5.2.0 
Contents 
1 Component History ................................ ................................ ................................ ........ 6 
2 Introduction ................................ ................................ ................................ .................... 7 
2.1 Architecture Overview ................................ ................................ .............................. 8 
3 Functional Description ................................ ................................ ................................ 10 
3.1 Features ................................ ................................ ................................ ................. 10 
3.2 Initialization ................................ ................................ ................................ ............ 11 
3.3 States ................................ ................................ ................................ ..................... 11 
3.4 Main Functions ................................ ................................ ................................ ....... 11 
3.5 Error Handling ................................ ................................ ................................ ........ 11 
3.5.1 Development Error Reporting ................................ ................................ ........ 11 
3.6 nPdu-to-Frame mapping for CAN-FD ................................ ................................ ..... 12 
4 Integration ................................ ................................ ................................ .................... 13 
4.1 Scope of Delivery ................................ ................................ ...................

### Page 4

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 4 
based on template version 5.2.0 
7.3 Limitations ................................ ................................ ................................ .............. 22 
8 Glossary and Abbreviations ................................ ................................ ........................ 23 
8.1 Glossary ................................ ................................ ................................ ................. 23 
8.2 Abbreviations ................................ ................................ ................................ ......... 24 
9 Contact................................ ................................ ................................ .......................... 25

### Page 5

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 5 
based on template version 5.2.0 
Illustrations 
Figure 2-1 AUTOSAR 4.1 Architecture Overview ................................ ......................... 8 
Figure 2-2 AUTOSAR architecture ................................ ................................ ............... 8 
Figure 2-3 Interfaces to adjacent modules of the IPDUM ................................ ............. 9 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 10 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 11 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 11 
Table 4-1 Static files ................................ ................................ ................................ . 13 
Table 4-2 Generated files ................................ ................................ ......................... 14 
Table 5-1 IpduM_InitMemory ................................ ................................ .................... 15 
Table 5-2 IpduM_Init ................................ ................................ ................................ . 16 
Table 5-3 IpduM_Transmit ................................ ................................ ........................ 16 
Table 5-4 IpduM_MainFunction ................................ ................................ ................ 17 
Table 5-5 IpduM_GetVersionInfo ................................ ................................ .............. 17 
Table 5-6 Services used by the IPDUM ...........................

### Page 6

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 6 
based on template version 5.2.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00  Component in conformance with AUTOSAR 3.2.1 
2.00  AUTOSAR 4.0.3 
2.01  BIG_ENDIAN copy segments 
2.02  Support post-build loadable 
3.00  Support post-build selectable 
 Support deleting container at post-build time 
4.00  Extend support for module initialization 
6.00  Support 16 bit selector 
 Support selector using more than one byte (i.e. crossing byte 
boundaries) 
6.01  Support nPdu-to-Frame Mapping for CAN-FD 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR I-PDU Multiplexer 
© 2016 Vector Informatik GmbH Version 2.06.00 7 
based on template version 5.2.0 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module IPDUM as specified in [1]. 
 
Supported AUTOSAR Release*: 4.x 
Supported Configuration Variants: PRE-COMPILE [SELECTABLE] 
POST-BUILD-LOADABLE [SELECTABLE] 
Vendor ID: IPDUM_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: IPDUM_MODULE_ID 52 decimal 
(according to ref. [2]) 
* For the precise AUTOSAR Release 4.x please see the release specific documentation. 
 
 
Multiplexing is a concept generally used to save CAN identifiers where an I-PDU with a 
CAN ID is used to carry different I-PDUs thereby saving the CAN IDs for the I-PDUs it 
carries. The IpduM can be used also with Flexray and LIN. 
 
I-PDU multiplexing means using the same PCI of a PDU with more than one unique 
layouts of its SDU. The SDU in a multiplexed I-PDU contains a selector field which 

*Excerpt: first 8 of 25 pages shown.*
