---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_E2EXf'
description: 'Converted PDF document TechnicalReference_E2EXf.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_E2EXf.pdf` (PDF, 612 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 23; title: MICROSAR E2E Transformer; author: Stephanie Schaaf

## Converted content

### Page 1

MICROSAR E2E Transformer 
Technical Reference 
 
 
Version 1.3.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Stephanie Schaaf 
Status Released

### Page 2

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Stephanie Schaaf 2016-10-21 1.0.0 Initial version 
Stephanie Schaaf 2017-03-21 1.1.0 Support for E2E profile 7 
Bernd Sigle 2017-06-06 1.2.0 Minor improvements 
Philipp Niethammer 2017-08-15 1.3.0 Updated to match Autosar 4.3.0 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_E2ETransformer.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 4.3.0 
[3] AUTOSAR AUTOSAR_SWS_DefaultErrorTracer.pdf 4.3.0 
[4] A AUTOSAR AUTOSAR_SWS_E2ELibrary.pdf 4.3.0 
Scope of the Document 
This technical reference describes the general use of the E2E Transformer. 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 3 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 Features ................................ ................................ ................................ ............ 9 
3.1.1 Deviations ................................ ................................ .......................... 9 
3.1.2 Additions/ Extensions ................................ ................................ ......... 9 
3.1.2.1 Memory Initialization ................................ ........................ 9 
3.1.3 Limitations ................................ ................................ ........................ 10 
3.2 Initialization ................................ ................................ ................................ ...... 10 
3.3 States ................................ ................................ ................................ .............. 10 
3.4 Main Functions ................................ ................................ ................................ 10 
3.5 Error Handling ................................ ................................ ................................ .. 10 
3.5.1 Development Error Reporting ................................ ..........................

### Page 4

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 4 
based on template version 6.0.1 
7.1 Glossary ................................ ................................ ................................ .......... 22 
7.2 Abbreviations ................................ ................................ ................................ ... 22 
8 Contact ................................ ................................ ................................ ........................ 23

### Page 5

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 5 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR Architecture Overview ................................ ............................... 7 
Figure 2-2 Interfaces to adjacent modules of the E2EXf ................................ .............. 8 
Figure 6-1 Configuration of EndToEndTransformationComSpecProps ....................... 21 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 9 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 9 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .... 9 
Table 3-4 Service IDs ................................ ................................ ............................... 10 
Table 3-5 Errors reported to DET ................................ ................................ ............. 11 
Table 4-1 Static files ................................ ................................ ................................ . 12 
Table 4-2 Generated files ................................ ................................ ......................... 12 
Table 5-1 E2EXf_ConfigType ................................ ................................ ................... 13 
Table 5-2 E2EXf_GetVersionInfo ................................ ................................ .............. 13 
Table 5-3 E2EXf_InitMemory ................................ ................................ .................... 14 
Table 5-4 E2EXf_Init ................................ ................................ ....

### Page 6

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 6 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.0.0 Initial creation 
1.1.0 Support for E2E profile 7 
1.2.0 Minor improvements 
1.3.0 Minor improvements 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 7 
based on template version 6.0.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module E2EXf as specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: pre-compile 
Vendor ID: E2EXf_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: E2EXf_MODULE_ID 176 decimal 
(according to ref. [2]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The E2EXf module provides the functionality to ensure a correct communication. 
2.1 Architecture Overview 
The following figure shows where the E2EXf is located in the AUTOSAR architecture. 
 
 
Figure 2-1 AUTOSAR Architecture Overview

### Page 8

Technical Reference MICROSAR E2E Transformer 
© 2017 Vector Informatik GmbH Version 1.3.0 8 
based on template version 6.0.1 
The next figure shows the interfaces to adjacent modules of the E2EXf. These interfaces 
are described in chapter 5. 
 
Figure 2-2 Interfaces to adjacent modules of the E2EXf 
 class Architecture
Det
E2ELibE2EXf

*Excerpt: first 8 of 23 pages shown.*
