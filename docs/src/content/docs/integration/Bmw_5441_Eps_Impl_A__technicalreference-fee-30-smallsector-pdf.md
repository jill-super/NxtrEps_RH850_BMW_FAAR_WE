---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Fee_30_SmallSector'
description: 'Converted PDF document TechnicalReference_Fee_30_SmallSector.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Fee_30_SmallSector.pdf` (PDF, 1041 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 42; title: MICROSAR [BSW module]; author: Michael Goß

## Converted content

### Page 1

MICROSAR Fee 
Technical Reference 
 
Small Sector 
Version 1.1.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Michael Goß 
Status Released

### Page 2

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
virgmi 2016-06-22 1.00.00 Initial version 
virgmi 2016-08-23 
 
2016-09-21 
1.01.00 Chapter ‘Requirements and 
Recommendations’ was added. 
Reference to ProductInformation of 
SmallSectorFee was added. 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_FlashEEPROMEmulation.pdf V2.0.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf V3.2.0 
[3] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[4] Vector ProductInformation_8_MICROSARSmallSectorFee.pdf V1.0.0 
 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 3 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ............................... 11 
3.1 Features ................................ ................................ ................................ .......... 11 
3.1.1 Deviations from AUTOSAR R4.0.3 ................................ ................... 11 
3.1.2 Additions/ Extensions ................................ ................................ ....... 12 
3.2 Recommendations ................................ ................................ ........................... 12 
3.3 Initialization ................................ ................................ ................................ ...... 13 
3.4 States ................................ ................................ ................................ .............. 13 
3.4.1 Module States ................................ ................................ .................. 13 
3.4.2 Job States ................................ ................................ ........................ 13 
3.5 Main Functions ................................ ................................ ................................ 14 
3.5.1 Processing of a Read Job ................................ ................................ 14 
3.5.2 Processing 

### Page 4

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 4 
based on template version 6.0.1 
5.2.5 Fee_30_SmallSector_Cancel ................................ ........................... 26 
5.2.6 Fee_30_SmallSector_GetStatus ................................ ...................... 26 
5.2.7 Fee_30_SmallSector_GetJobResult ................................ ................ 27 
5.2.8 Fee_30_SmallSector_InvalidateBlock ................................ .............. 28 
5.2.9 Fee_30_SmallSector_GetVersionInfo ................................ .............. 29 
5.2.10 Fee_30_SmallSector_EraseImmediateBlock ................................ ... 29 
5.2.11 Fee_30_SmallSector_MainFunction ................................ ................ 30 
5.2.12 Fee_30_SmallSector_SuspendWrites ................................ .............. 31 
5.2.13 Fee_30_SmallSector_ResumeWrites ................................ ............... 31 
5.3 Services used by FEE ................................ ................................ ...................... 32 
5.4 Callback Functions ................................ ................................ ........................... 32 
5.4.1 Fee_30_SmallSector_JobEndNotification ................................ ........ 32 
5.4.2 Fee_30_SmallSector_JobErrorNotification ................................ ....... 33 
5.5 Configurable Interfaces ................................ ................................ .................... 34 
6 Configuration ................................ ................................ ................................ .............. 35 
6.1 Configuration Variants ................................ ................................ ...................... 35 
6.2 Configuration with DaVinci Configurator ................

### Page 5

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 5 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 8 
Figure 2-2 AUTOSAR 3.x Architecture Overview ................................ ......................... 9 
Figure 2-3 Interfaces to adjacent modules of the FEE ................................ ............... 10 
Figure 4-1 Update references of BSWMD file ................................ ............................ 21 
Figure 4-2 Example PartitionConfiguration after updating BSWMD references .......... 21 
Figure 4-3 DaVinci Configurator signals incorrect definition of configuration 
elements ................................ ................................ ................................ ... 22 
Figure 4-4 Choose solving action to delete all erroneous definitions .......................... 22 
Figure 6-1 Configuring FeeFlsApi container ................................ ............................... 36 
Figure 6-2 SmallSectorFee Partition Configuration example (RH850)........................ 36 
Figure 6-3 Block Configuration................................ ................................ ................... 37 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 11 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 12 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 12 
Table 3-4 Module States ................................ ................................ ..........................

### Page 6

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 6 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Initial version of SmallSectorFee 
1.01.00 Chapter ‘Requirements and Recommendations’ was added 
Reference to SmallSectorFee’s ProductInformation was added 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR Fee 
© 2016 Vector Informatik GmbH Version 1.1.0 7 
based on template version 6.0.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSA R BSW 
module FEE as specified in [1]. 
 
Supported AUTOSAR Release*: 3, 4 
Supported Configuration Variants: pre-compile 
Vendor ID: FEE_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: FEE_MODULE_ID 21 decimal 
(according to ref. [3]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The FEE enables you to access a dedicated flash area for storing data persistently. It is 
intended to be used exclusively either by the NVRAM Manager or on SW instance within a 
Flash-Boot-Loader. 
This module is especially designed for Flash devices with small sector and page sizes, 
e.

*Excerpt: first 8 of 42 pages shown.*
