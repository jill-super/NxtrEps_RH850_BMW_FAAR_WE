---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_VStdLib_GenericAsr'
description: 'Converted PDF document TechnicalReference_VStdLib_GenericAsr.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_VStdLib_GenericAsr.pdf` (PDF, 657 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 26; title: MICROSAR VStdLib; author: Torsten Kercher

## Converted content

### Page 1

MICROSAR VStdLib 
Technical Reference 
 
Generic implementation of the Vector Standard Library 
Version 1.00.01 
 
 
 
 
 
 
 
 
 
 
 
Authors Torsten Kercher 
Status Released

### Page 2

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 2 
based on template version 5.9.0 
Document Information 
 
History 
Author Date Version Remarks 
Torsten Kercher 2015-05-04 1.00.00 Creation 
Torsten Kercher 2016-04-12 1.00.01 Update to new CI, no changes in content 
 
 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 1.6.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf 3.2.0 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 3 
based on template version 5.9.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 5 
2 Introduction................................ ................................ ................................ ................... 6 
2.1 Architecture Overview ................................ ................................ ........................ 6 
3 Functional Description ................................ ................................ ................................ . 8 
3.1 Features ................................ ................................ ................................ ............ 8 
3.2 Initialization and Main Functions ................................ ................................ ........ 8 
3.3 Error Handling ................................ ................................ ................................ .... 8 
4 Integration ................................ ................................ ................................ ..................... 9 
4.1 Scope of Delivery ................................ ................................ ............................... 9 
4.2 Include Structure ................................ ................................ ................................ 9 
4.3 Critical Sections ................................ ................................ ................................ . 9 
4.4 Compiler Abstraction and Memory Mapping ................................ ..................... 10 
4.5 Integration Hints ................................ ................................ ............................... 11 
5 API Description ..............................

### Page 4

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 4 
based on template version 5.9.0 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 6 
Figure 2-2 Interfaces to adjacent modules ................................ ................................ ... 7 
Figure 4-1 Include Structure ................................ ................................ ........................ 9 
 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 5 
Table 3-1 Service IDs ................................ ................................ ................................ . 8 
Table 3-2 Errors reported to DET ................................ ................................ ............... 8 
Table 4-1 Static files ................................ ................................ ................................ ... 9 
Table 4-2 Compiler Abstraction and Memory Mapping ................................ ............. 10 
Table 5-1 VStdLib_GetVersionInfo ................................ ................................ ........... 12 
Table 5-2 VStdLib_MemClr ................................ ................................ ...................... 13 
Table 5-3 VStdLib_MemClrMacro ................................ ................................ ............. 14 
Table 5-4 VStdLib_MemSet ................................ ................................ ...................... 15 
Table 5-5 VStdLib_MemSetMacro ................................ ................................ ............ 16 
Table 5-6 VStdLib_MemCpy ................................ ................................ ..................... 17 
Table 5-7 VStdLib_Me

### Page 5

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 5 
based on template version 5.9.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00 Creation of the component. 
2.00 Detach the component from core-based implementations, give optimized 
routines and support operations on large data (> 65535 bytes). 
Table 1-1 Component history

### Page 6

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 6 
based on template version 5.9.0 
2 Introduction 
This document describes the functionality, API and configuration of the generic Vector 
Standard Library (VStdLib). 
 
Supported AUTOSAR Release*: 4.x 
Supported Configuration Variants: pre-compile 
Vendor ID: VSTDLIB_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: VSTDLIB_MODULE_ID 255 decimal 
(according to [1]) 
* For the precise AUTOSAR Release 4.x please see the release specific documentation. 
 
The VStdLib provide s a hardware independent implementation of memory manipulation 
services used by several MICROSAR BSW components. 
2.1 Architecture Overview 
The following figure shows where the VStdLib is located in the AUTOSAR architecture. 
 
Figure 2-1 AUTOSAR 4.x Architecture Overview

### Page 7

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 7 
based on template version 5.9.0 
The next figure shows the interfaces to adjacent modules of the VStdLib. These interfaces 
are described in chapter 5. 
 
Figure 2-2 Interfaces to adjacent modules 
 
 
 class Module Structure
«EmbeddedInterface»
VStdLib
+ VStdLib_GetVersionInfo()
+ VStdLib_MemClr()
+ VStdLib_MemClrLarge()
+ VStdLib_MemClrMacro()
+ VStdLib_MemCpy()
+ VStdLib_MemCpy_s()
+ VStdLib_MemCpy16()
+ VStdLib_MemCpy16Large()
+ VStdLib_MemCpy32()
+ VStdLib_MemCpy32Large()
+ VStdLib_MemCpyLarge()
+ VStdLib_MemCpyLarge_s()
+ VStdLib_MemCpyMacro()
+ VStdLib_MemCpyMacro_s()
+ VStdLib_MemSet()
+ VStdLib_MemSetLarge()
+ VStdLib_MemSetMacro()
Module
Det
Module
MICROSAR BSW
module
Module
VStdLib
«EmbeddedInterface»
Det
+ Det_ReportError()
Module
(Compiler) Library
«EmbeddedInterface»
(Compiler) Library«us e
optionally»
«realize»
«us e»
«us e
optionally»
«realize»
«realize»

### Page 8

Technical Reference MICROSAR VStdLib 
© 2016 Vector Informatik GmbH Version 1.00.01 8 
based on template version 5.9.0 
3 Functional Description 
This chapter describes the general function of the component. 
3.1 Features 
The Vector Standard Library gives a standard interface for memory initialization and copy 
services as described in section 5.2. It provides a hardware independent implementation 
of this interface , but also allows the mapping to project specific impl ementations for 
optimization reasons. 
3.2 Initialization and Main Functions 
No initialization is necessary and no main functions are provided. 
3.3 Error Handling 
3.3.1 Development Error Reporting 
By default, development errors are reported to the DET using the service 
Det_ReportError() as specified in [2], if development error reporting is enabled (i.e. 
pre-compile parameter VSTDLIB_DEV_ERROR_REPORT == STD_ON). 
If another module is used for development error reporting,

*Excerpt: first 8 of 26 pages shown.*
