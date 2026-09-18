---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_ComXf'
description: 'Converted PDF document TechnicalReference_ComXf.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_ComXf.pdf` (PDF, 562 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 15; title: MICROSAR COM Based Transformer; author: Cornelius Reuss, Sascha Sommer, Katharina Benkert

## Converted content

### Page 1

MICROSAR COM Based Transformer 
Technical Reference 
 
 
Version 1.8.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Cornelius Reuss, Sascha Sommer, Katharina Benkert 
Status Released

### Page 2

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Cornelius Reuss 2015-07-07 1.0.0 Initial version 
Cornelius Reuss 2016-02-26 1.1.0 New Layout 
Sascha Sommer 2016-05-17 1.2.0 Version update only 
Sascha Sommer 2016-05-17 1.3.0 Version update only 
Cornelius Reuss 2016-06-23 1.4.0 Version update only 
Katharina Benkert 2016-11-17 1.5.0 Version update only 
Bernd Sigle 2017-03-20 1.6.0 Version update only 
Bernd Sigle 2017-06-06 1.7.0 Version update only 
Bernd Sigle 2017-08-17 1.8.0 Support for AUTOSAR 4.3.0 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_COMBasedTransformer.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 4.3.0 
[3] AUTOSAR AUTOSAR_SWS_COM.pdf 4.3.0 
Scope of the Document 
This technical reference describes the general use of the COM Based Transformer. 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 3 
based on template version 5.12.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 5 
2 Introduction................................ ................................ ................................ ................... 6 
2.1 Architecture Overview ................................ ................................ ........................ 6 
3 Functional Description ................................ ................................ ................................ . 7 
3.1 Features ................................ ................................ ................................ ............ 7 
3.1.1 Deviations ................................ ................................ .......................... 7 
3.2 Initialization ................................ ................................ ................................ ........ 7 
3.3 States ................................ ................................ ................................ ................ 7 
3.4 Main Functions ................................ ................................ ................................ .. 7 
3.5 Error Handling ................................ ................................ ................................ .... 7 
3.5.1 Development Error Reporting ................................ ............................. 7 
3.5.2 Production Code Error Reporting ................................ ....................... 8 
4 Integration ................................ ................................ ................................ ..................... 9 
4.1 Scope of Delivery ................................ .

### Page 4

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 4 
based on template version 5.12.0 
Illustrations 
Figure 2-1 AUTOSAR Architecture Overview ................................ ............................... 6 
Figure 6-1 Enable Data Transformation ................................ ................................ ..... 13 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 5 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 7 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 7 
Table 4-1 Static files ................................ ................................ ................................ ... 9 
Table 4-2 Generated files ................................ ................................ ........................... 9 
Table 5-1 ComXf_Init ................................ ................................ ................................ 10 
Table 5-2 ComXf_DeInit ................................ ................................ ........................... 10 
Table 5-3 ComXf_GetVersionInfo ................................ ................................ ............. 11 
Table 5-4 ComXf_<transformerId> ................................ ................................ ........... 11 
Table 5-5 ComXf_Inv_<transformerId> ................................ ................................ ..... 12 
Table 7-1 Glossary ................................ ................................ ................................ ... 14 
Table 7-2 Abbreviations ................................ ................................ ............................ 14

### Page 5

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 5 
based on template version 5.12.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.0.0 Initial Creation 
1.2.0 Version update only 
1.3.0 Version update only 
1.4.0 Version update only 
1.5.0 MISRA enhancements 
1.6.0 Version update only 
1.7.0 Version update only 
1.8.0 Support of AUTOSAR 4.3.0 
Table 1-1 Component history

### Page 6

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 6 
based on template version 5.12.0 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module ComXf as specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: pre-compile 
Vendor ID: COMXF_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: COMXF_MODULE_ID 175 decimal 
(according to ref. [2]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The ComXf module provides the functionality to serialize complex data when the target 
bus system uses a fixed communication matrix. 
2.1 Architecture Overview 
The following figure shows where the ComXf is located in the AUTOSAR architecture. 
 
Figure 2-1 AUTOSAR Architecture Overview

### Page 7

Technical Reference MICROSAR COM Based Transformer 
© 2017 Vector Informatik GmbH Version 1.8.0 7 
based on template version 5.12.0 
3 Functional Description 
3.1 Features 
The features listed in th e following tables cover the complete functionality specified for the 
ComXf. 
The AUTOSAR standard functionality is speci fied in [1], the corresponding features are 
listed in the tables 
> Table 3-1 Supported AUTOSAR standard conform features 
> Table 3-2 Not supported AUTOSAR standard conform features 
 
The following features specified in [1] are supported: 
Supported AUTOSAR Standard Conform Features 
Serialization / Deserialization of complex data for S/R communication. 
Table 3-1 Supported AUTOSAR standard conform features 
3.1.1 Deviations 
The following features specified in [1] are not supported: 
Not Supported AUTOSAR Standard Conform Features 
Development error detection. 
Postbuild support. 
Table 3-2 Not supported AUTOSAR standard conform features 
3.2 Initialization 
The ComXf does not have to be initialized or deinitialized. Calls to ComXf_Init() and 
ComXf_DeInit() can be omitted. 
3.3 States 
No internal states exist. 
3.4 Main Functions 
No main function exists because all functionality is performed within the called API. 
3.5 Error Handling 
3.5.1 Development Error Reporting 
No development error reporting is currently supported by ComXf.

### Page 8

Technical 

*Excerpt: first 8 of 15 pages shown.*
