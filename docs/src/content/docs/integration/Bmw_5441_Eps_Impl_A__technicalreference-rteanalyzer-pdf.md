---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_RteAnalyzer'
description: 'Converted PDF document TechnicalReference_RteAnalyzer.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_RteAnalyzer.pdf` (PDF, 727 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 30; title: MICROSAR RTE Analyzer; author: Sascha Sommer

## Converted content

### Page 1

MICROSAR RTE Analyzer 
Technical Reference 
 
 
Version 1.0.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Sascha Sommer 
Status Released

### Page 2

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Sascha Sommer 2015-09-25 0.5 Initial creation for RTE Analyzer 0.5.0 
Sascha Sommer 2016-02-26 0.6 Update for RTE Analyzer 0.6.0 
Sascha Sommer 2016-07-07 0.7 Described Configuration Feedback and 
Template Variant Check 
Sascha Sommer 2016-10-20 0.8 Configuration Feedback extensions 
Sascha Sommer 
Charu Pathni 
2017-03-23 0.9 Updated for RTE Analyzer 0.9.0 
Removed BETA disclaimer 
Fixed chapter numbering 
Sascha Sommer 2017-05-09 1.0 Update for RTE Analyzer 1.0.0 
Reference Documents 
No. Source Title Version 
[1] ISO ISO/IEC 9899:1990, Programming languages -C Second 
edition 
[2] AUTOSAR AUTOSAR_SWS_RTE.pdf 4.2.2 
 
 
Scope of the Document 
This technical reference describes the general use of the MICROSAR RTE Analyzer static 
code analysis tool. This document is relevant for developers that want to integrate a 
generated RTE into an ECU with functional safety requirements. All aspects that concern 
the generation of the RTE are described in the technical reference of the RTE. 
 
 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 3 
based on template version 5.12.0

### Page 4

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 4 
based on template version 5.12.0 
Contents 
 
1 RTE Analyzer History ................................ ................................ ................................ ... 6 
2 Introduction................................ ................................ ................................ ................... 7 
3 Functional Description ................................ ................................ ................................ . 8 
4 RTE Analysis and Integration ................................ ................................ .................... 10 
4.1 Scope of Delivery ................................ ................................ ............................. 10 
4.1.1 Static Files ................................ ................................ ....................... 10 
4.1.2 Dynamic Files ................................ ................................ .................. 12 
4.2 Restrictions ................................ ................................ ................................ ...... 13 
4.3 RTE Analyzer Command Line Options ................................ ............................. 13 
4.4 Analysis Report Contents ................................ ................................ ................. 14 
4.4.1 Analyzed Files ................................ ................................ .................. 14 
4.4.2 Configuration Parameters ................................ ................................ 14 
4.4.3 Findings ................................ ................................ ........................... 15 
4.4.4 Configuration Feedback ................................ ................................ ... 22 
4.4.5 Template Variant Check

### Page 5

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 5 
based on template version 5.12.0 
Tables 
Table 1-1 RTE Analyzer history ................................ ................................ .................. 6 
Table 3-1 Supported features ................................ ................................ .................... 9 
Table 4-1 Static files ................................ ................................ ................................ . 11 
Table 4-2 Assumed platform type sizes ................................ ................................ .... 12 
Table 4-3 Generated files ................................ ................................ ......................... 13 
Table 4-4 RTE Analyzer Command Line Options ................................ ...................... 14 
Table 4-5 Analysis parameters that are extracted from the configuration .................. 15 
Table 4-6 RTE Analyzer Findings ................................ ................................ ............. 22 
Table 5-1 Glossary ................................ ................................ ................................ ... 28 
Table 5-2 Abbreviations ................................ ................................ ............................ 28 
Table 6-1 Free and Open Source Software Licenses ................................ ............... 29 
Figures 
Figure 4-1 Project menu ................................ ................................ ............................ 25 
Figure 4-2 External generation steps ................................ ................................ ......... 25 
Figure 4-3 Code generation ................................ ................................ ....................... 26

### Page 6

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 6 
based on template version 5.12.0 
1 RTE Analyzer History 
The RTE Analyzer history gives an overview over the important milestones that are 
supported in the different versions of the RTE Analyzer. 
RTE Analyzer 
Version 
New Features 
0.5.0 Initial version of MICROSAR RTE Analyzer for MICROSAR RTE 4.9.x 
Supported Features: 
- Detection of RTE code that cannot be compiled 
- Detection of Out Of Bounds write accesses within RTE APIs 
- Detection of Interrupt Lock API sequence mismatches within RTE 
APIs 
- Detection of Unreachable RTE APIs and runnables 
- Detection of RTE variables that are accessed from concurrent 
execution contexts without protection 
- Detection of concurrent calls to non-reentrant APIs within the RTE 
- Detection of variables that are accessed from multiple cores and 
that are not mapped to non-cacheable memory sections 
- Detection of non-typesafe interfaces to the BSW and SWCs where 
a call with a wrong parameter might cause out of bounds writes by 
the RTE or a called runnable/BSW API. 
- Detection of recursive call sequences 
0.6.0 Updated for MICROSAR RTE 4.10.x 
0.6.1 Updated for MICROSAR RTE 4.11.x 
0.7.0 Updated for MICROSAR RTE 4.12.x 
New optimized Range Analysis algorithm 
Added Configuration Feedback 
Added Template Variant Check 
0.8.0 Extended Configuration Feedback 
Findings that are expected to always occur were moved to the 
configuration feedback section in the Analysis report 
RTE Analyzer now automatically extracts the number of bytes written by 
the COM signal reception APIs from the generated MICROSAR COM 
sources 
RTE Analyzer now automatically extracts the size of the buffer that is 
passed by the NVM module from the generated MICROSAR

### Page 7

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH Version 1.0.0 7 
based on template version 5.12.0 
2 Introduction 
This document describes the static code analysis tool MICROSAR RTE Analyzer. 
MICROSAR RTE Analyzer is part of MICROSAR Safe RTE. MICROSAR Safe RTE 
provides an AUTOSAR RTE generator that is developed with a n ISO26262 compliant 
development process, to allow the usage of the generated RTE code within an ECU with 
functional safety requirements. 
MICROSAR RTE Analyzer analyzes the generated RTE code for errors with a special 
emphasis on sporadic runtime errors that are hard to detect during ECU integration tests.

### Page 8

Technical Reference MICROSAR RTE Analyzer 
© 2017 Vector Informatik GmbH 

*Excerpt: first 8 of 30 pages shown.*
