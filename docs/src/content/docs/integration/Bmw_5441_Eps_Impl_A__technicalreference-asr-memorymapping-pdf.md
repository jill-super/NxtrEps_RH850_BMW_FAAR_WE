---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Asr_MemoryMapping'
description: 'Converted PDF document TechnicalReference_Asr_MemoryMapping.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Asr_MemoryMapping.pdf` (PDF, 446 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 20; title: MICROSAR Memory Mapping; author: Eugen Stripling

## Converted content

### Page 1

MICROSAR Memory Mapping 
Technical Reference 
 
 
Version 1.3.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Eugen Stripling 
Status Released

### Page 2

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 2 
based on template version 5.6.0 
Document Information 
History 
Author Date Version Remarks 
Eugen Stripling 2013-04-12 1.00.00 Creation - ESCAN00064655 
Eugen Stripling 2013-05-29 1.00.01 Some typos corrected 
Eugen Stripling 2016-09-27 1.01.00 FEATC-317 / FEAT-2002: 64-bit memory 
section keywords added 
Eugen Stripling 2017-01-16 1.02.00 ESCAN00093572: 2.1.4 chapter added 
Eugen Stripling 2017-07-18 1.03.00 Chapters 2.1 and 2.1.4 adapted due to 
ESCAN00095756 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_MemoryMapping.pdf 1.4.0 
[2] AUTOSAR AUTOSAR_SWS_MemoryMapping.pdf 4.2.2 
[3] AUTOSAR AUTOSAR_SWS_CompilerAbstraction.pdf 3.2.0 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 3 
based on template version 5.6.0 
Contents 
1 Introduction................................ ................................ ................................ ................... 5 
2 Functional Description ................................ ................................ ................................ . 6 
2.1 Memory section keywords ................................ ................................ .................. 6 
2.1.1 Declaration of code and data segments in AUTOSAR ........................ 7 
2.1.2 Mapping of code and data segments to a dedicated memory area ..... 8 
2.1.3 Example: Mapping of data to a post-build memory section................. 9 
2.1.4 Usage of AUTOSAR 4.2.2 BSW module ................................ .......... 11 
3 Appendix ................................ ................................ ................................ ..................... 12 
3.1 Sub-keywords used in the memory section and compiler specific keywords .... 12 
3.2 Memory section keywords ................................ ................................ ................ 12 
3.2.1 Memory section keywords for code ................................ .................. 13 
3.2.2 Memory section keywords for constants ................................ ........... 13 
3.2.3 Memory section keywords for variables................................ ............ 14 
3.3 Compiler specific keywords ................................ ................................ .............. 17 
4 Glossary and Abbreviations ................................ ................................ ...................... 19 
4.1 Abbreviations ................................ ................................ .................

### Page 4

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 4 
based on template version 5.6.0 
Illustrations 
Figure 2-1 Files: MemMap.h, MemMap_Common.h and Compiler_Cfg.h ................... 7 
 
Tables 
Table 3-1 Explanation of sub-keywords used in the memory section and compiler 
specific keywords ................................ ................................ ..................... 12 
Table 3-2 Memory sections for code ................................ ................................ ......... 13 
Table 3-3 Memory sections for constants ................................ ................................ . 13 
Table 3-4 Change of memory section keywords for constants in ASR 4.0.3 ............. 14 
Table 3-5 Memory sections for variables ................................ ................................ .. 15 
Table 3-6 Change of memory section keywords for variables in ASR 4.0.3 .............. 17 
Table 3-7 Compiler specific keywords and the related memory sections they used 
for ................................ ................................ ................................ ............. 18 
Table 4-1 Abbreviations ................................ ................................ ............................ 19

### Page 5

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 5 
based on template version 5.6.0 
1 Introduction 
This document gives an overview about the functionality of memory mapping as specified 
by AUTOSAR according to the Vector specific implementation (MICROSAR).

### Page 6

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 6 
based on template version 5.6.0 
2 Functional Description 
In the following chapters the following two expressions are used: 
 memory section keyword 
and 
 memory area. 
A memory section keyword describes a memory section according to AUTOSAR 
symbolically. All available corresponding keywords are described in chapter 3.2. By 
memory area a memory section in hardware at all is meant. 
By using of expression build-toolchain the functionality covered by a comp iler, linker and 
locator is meant. 
In addition the abb reviations MSN1 and Msn1 respectively are used as placeholders for the 
short name of any BSW module. However AUTOSAR itself prefer s to use the 
abbreviations MIP2 and Mip2 respectively. Both abbreviations mean the same. 
2.1 Memory section keywords 
The keywords of memory sections of all BSW modules which are implemented acco rding 
to AUTOSAR 4.0.3 are located in the file MemMap.h. BSW modules implemented 
according to AUTOSAR 4.0.3 include this general file. However BSW modules which are 
implemented according to AUTOSAR 4.2.2 have their own specific <Msn>_MemMap.h file 
and include generally only their own file. For more information about usage of BSW 
modules which are implemented according to AUTOSAR 4.2.2 please see chapter 2.1.4. 
The file Compiler_Cfg.h contains additional compiler specific keywords. These 
keywords are used to describe t he memory location of variables, constants and pointers. 
In case of pointer s additional keywords are defined to describe the memory location t he 
pointer points to. 
All files are provided as templates and may be modified and extended by the user if 
required. The files MemMap.h and Compiler_Cfg.h are named _MemMap.h an

### Page 7

Technical Reference MICROSAR Memory Mapping 
© 2017 Vector Informatik GmbH Version 1.3.0 7 
based on template version 5.6.0 
 
Figure 2-1 Files: MemMap.h, MemMap_Common.h and Compiler_Cfg.h 
 
Each BSW module has its own set of compiler specific and memory section keywords with 
the pre-fix <MSN>. By default all the memory section keywords are mapped to the same 
default memory section keyword defined in file MemMap_Common.h. If required the default 
mapping can be modified by the BSW integrator. Detailed information concerning the 
provided memory section keywords can be found in the chapter 3.2. For detailed 
information about the compiler specific keywords please see the chapter 3.3. 
 
2.1.1 Declaration of code and data segments in AUTOSAR 
The declaration of all kinds of variables including constants, pointers and the code itself is 
performed in the following way. 
1. Opening of the memory section: The memory section where e.g. a variable shall 
be stored in is opened by defining of the corresponding memory section keyword 
(s. chapter 3.2). 
2. Including of file MemMap.h/<Msn>_MemMap.h: In this step the previously defined 
BSW module specific memory section keyword is redefined to the default keyword 
of the corresponding memory section. Additionally if specified the corresponding 
#pragma-command is activated. This command tells the build-toolchain to put the 
following data or code segments to intended memory area. 
3. Declaration of data and code segments: In t

*Excerpt: first 8 of 20 pages shown.*
