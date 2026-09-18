---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_ComStackLib'
description: 'Converted PDF document TechnicalReference_ComStackLib.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_ComStackLib.pdf` (PDF, 737 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 41; title: MICROSAR ComStackLib; author: Gunnar Meiss

## Converted content

### Page 1

MICROSAR ComStackLib 
Technical Reference 
 
ComStackLib based BSW generators 
Version 2.01.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Gunnar Meiss 
Status Released

### Page 2

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 2 
based on template version 5.5.0 
Document Information 
History 
Author Date Version Remarks 
Gunnar Meiss 2013-03-25 1.00.00 initial version 
Gunnar Meiss 2013-08-23 1.01.00 ESCAN00068919 Remove 
<MSN>UseSignedDataTypesInIndexArrays 
ESCAN00070017 Remove <MSN>_Resource.xml 
Gunnar Meiss 2014-10-06 2.00.00 ESCAN00078776 AR4-698: Post-Build Selectable 
(Identity Manager) 
Gunnar Meiss 2014-12-19 2.00.01 ESCAN00080380 Minor typing and grammar corrections 
Gunnar Meiss 2016-03-30 2.00.02 ESCAN00089127 Extend MD_CSL_3355_3356 with the 
aspects of the PRQA Rule 3358 and 3359 
ESCAN00089126 Support a justification for PRQA Rule 
310 and PCSymbolicNonDereferenciateablePointers 
Added chapter Freedom from Interference 
Gunnar Meiss 2016-07-19 2.00.03 ESCAN00091055 Extend 
MD_CSL_3355_3356_3358_3359 with the aspects of 
PRQA Rule 3325 
Gunnar Meiss 2017-03-24 2.01.00 STORYC-534: <MSN>MinimizeNumericalDataTypes is 
always enabled 
Reference Documents 
No. Source Title Version 
[1] Vector Compliance Documentation MISRA-C:2004 / MICROSAR 2.2.0 
Scope of the Document 
This technical reference describes the general use of the ComStackLib based BSW 
generators.

### Page 3

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 3 
based on template version 5.5.0 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 4 
based on template version 5.5.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 CONFIG-CLASS of Data ................................ ................................ .................. 10 
3.2 CONFIG-CLASS PRE-COMPILE Optimizations ................................ .............. 10 
3.2.1 Optimize Const Data to Defines ................................ ....................... 10 
3.2.2 Optimize Bool Data in Structs ................................ .......................... 11 
3.2.3 Data Deduplication and Reduction ................................ ................... 12 
3.2.3.1 Equal Data ................................ ................................ ..... 13 
3.2.3.2 Unary and Binary Operations ................................ ......... 14 
3.2.4 Data Streaming ................................ ................................ ................ 15 
3.3 CONFIG-CLASS Independent Optimizations ................................ ................... 16 
3.3.1 Sort Struct Elements ................................ ................................ ........ 16 
3.3.2 Optimize Data Types ................................ ................................ ........ 17 
3.4 SELECTABLE Optimizations .......................

### Page 5

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 5 
based on template version 5.5.0 
Illustrations 
Figure 2-1 Embedded Code Aspects ................................ ................................ ........... 7 
Figure 2-2 AUTOSAR 4.2 Architecture Overview ................................ ......................... 8 
Figure 3-1 Resources in compiler optimization variants ................................ ............... 9 
Figure 3-2 Using defines for CONST data ................................ ................................ .. 10 
Figure 3-3 Boolean struct data variants ................................ ................................ ..... 11 
Figure 3-4 Boolean struct data versus Bitmasking ................................ ..................... 12 
Figure 3-5 Data deduplication without operations ................................ ...................... 13 
Figure 3-6 Data deduplication with operations ................................ ........................... 14 
Figure 3-7 Data Streaming ................................ ................................ ......................... 15 
Figure 3-8 Sorting struct elements ................................ ................................ ............. 16 
Figure 3-9 Data type minimization ................................ ................................ ............. 17 
Figure 4-1 Resources in optimization variants ................................ ........................... 22 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 4-1 Generated files ................................ ................................ ......................... 20 
Table 4-2 IMPLEMENTATION-CONFIG-VARIATIONS ............

### Page 6

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 6 
based on template version 5.5.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Support of embedded data generation in the 
IMPLEMENTATION-CONFIG-VARIANT VARIANT-PRE-COMPILE 
2.00.00 Support of the 
IMPLEMENTATION-CONFIG-VARIANT VARIANT-POST-BUILD-
LOADABLE 
3.00.00 Revision of existing techniques 
4.00.00 Revision of existing techniques 
5.00.00 AR4-698: Post-Build Selectable (Identity Manager) 
6.00.00 Support VTT 
7.00.00 Support Techniques to ensure Freedom of Interference 
8.00.00 Java 8 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 7 
based on template version 5.5.0 
2 Introduction 
This document describes the configuration of ComStackLib based BSW generators. 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: PRE-COMPILE [SELECTABLE] 
POST-BUILD-LOADABLE [SELECTABLE] 
* For the precise AUTOSAR Release 4.x please see the release specific documentation. 
 
The ComStackLib is an embedded data generation engine designed for AUTOSAR based 
BSW software. Generating embe dded software is situated in the context of different 
aspects. 
 
 
Figure 2-1 Embedded Code Aspects 
The number of aspects for embedded software is quite high and they have a various 
importance from the view of different stakeholders. Some aspects contradict to each other 
and other aspects cannot be changed at the time of the project. Due to this the 
ComStackLib has been introduced as scalable embedded data generation engine 
designed for AUTOSAR. 
 
 
 
Size of ROM
Size of RAM
Size of code
Runtime of code
Readability of code
Readability of generated
data
MISRA conformanceMaintainability of the BSW
and code generators
Hardware
Compiler implementations
and configurations
Complexity of Features
Complexity of different
configuration variants
Development costs
Developer Customer A Customer B

### Page 8

Technical Reference MICROSAR ComStackLib 
© 2017 Vector Informatik GmbH Version 2.01.00 8 
based on template version 5.5.0 
2.1 Architecture Overview 
The following figure shows where the ComStackLib is used in the MICROSAR 
architecture. 
 
Figure 2-2 AUTOSAR 4.2 Architecture Overview

*Excerpt: first 8 of 41 pages shown.*
