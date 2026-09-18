---
title: 'TL102A_Davinci — TechnicalReference_DataTypes_AR4'
description: 'Converted PDF document TechnicalReference_DataTypes_AR4.pdf from module TL102A_Davinci.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_DataTypes_AR4.pdf` (PDF, 3864 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 80; title: Autosar 4.0 - DataTypes; author: Thomas Bruni

## Converted content

### Page 1

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
1 / 80 
 
 
 
 
 
 
 
 
 
 
 
Autosar 4.0 - DataTypes 
Technical Reference 
 
 
Version 1.1 
 
 
 
 
 
 
 
 
 
 
Authors Thomas Bruni 
Status Released

### Page 2

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
2 / 80 
Document Information 
History 
Author Date Version Remarks 
Thomas Bruni 11.11.2013 0.1 Document creation 
Thomas Bruni 14.01.2014 0.2 Changes: 
3.4 Platform types 
 
Thomas Bruni 27.01.2014 0.3 Corrections in 3.4 Platform 
types 
Thomas Bruni 29.01.2014 0.4 Creation of 2 new chapter s: 
3.4 Data type mapping 
5.4 Data type mapping 
assistant 
5.5 Type emitter 
Thomas Bruni 21.02.2014 1.0 Release version 
Thomas Bruni 14.03.2014 1.1 Changes for Mode 
Declaration Group mapping : 
chapters 3.4 and 4.4. 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_TPS_SoftwareComponentTemplate 4.2.0 
[2] AUTOSAR AUTOSAR_SWS_PlatformTypes 2.5.0

### Page 3

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
3 / 80 
Contents 
1 Introduction ................................ ................................ ................................ .................... 6 
2 Data Types and Data Prototypes ................................ ................................ ................... 7 
3 Design of data prototypes in DaVinci tool chain ................................ .......................... 8 
3.1 Data prototypes ................................ ................................ ................................ ........ 8 
3.2 Application data types ................................ ................................ ............................ 10 
3.3 Implementation data types ................................ ................................ ..................... 11 
3.4 Data type mapping ................................ ................................ ................................ . 14 
3.5 Platform types ................................ ................................ ................................ ........ 15 
3.5.1 Definitions ................................ ................................ ................................ ..... 15 
3.5.1.1 Autosar Standard Types ................................ ................................ ......... 15 
3.5.1.2 Platform Types ................................ ................................ ....................... 15 
3.5.1.3 Valid C expression ................................ ................................ .................. 15 
3.5.2 Practice ................................ ................................ ................................ ......... 16 
3.5.2.1 Abstraction of SW from platform ...........

### Page 4

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
4 / 80 
5.5 Type emitter ................................ ................................ ................................ ........... 78 
6 Glossary and Abbreviations ................................ ................................ ........................ 79 
6.1 Glossary ................................ ................................ ................................ ................. 79 
6.2 Abbreviations ................................ ................................ ................................ ......... 79 
7 Contact................................ ................................ ................................ .......................... 80 
 
Illustrations 
Figure 3-1 S/R port interface element ................................ ................................ .......... 9 
Figure 3-2 S/R port interface element init value ................................ ........................... 9 
Figure 3-3 DaVinci Developer – workspace library ................................ ..................... 10 
Figure 3-4 Application data type categories ................................ ............................... 10 
Figure 3-5 Application data type Value property dialog ................................ .............. 11 
Figure 3-6 Implementation data type categories ................................ ........................ 12 
Figure 3-7 Implementation data type Value property dialog ................................ ....... 13 
Figure 3-8 2 ways of modelling platform independent implementation data types ...... 17 
Figure 3-9 Modelling a platform specific implementation data type ............................ 18 
Figure 3-10 Platform Types in DaVi

### Page 5

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
5 / 80 
Figure 4-29 My_Enumeration type ................................ ................................ ............... 48 
Figure 4-30 My_EnumerationType_CompuMethod ................................ ...................... 49 
Figure 4-31 Enumeration text table setting ................................ ................................ .. 49 
Figure 4-32 Enumeration constraint ................................ ................................ ............. 50 
Figure 4-33 My_Enumeration mapping to uint8 ................................ ........................... 50 
Figure 4-34 “My_EnumerationInterface” ................................ ................................ ...... 50 
Figure 4-35 My_EnumerationImplType ................................ ................................ ........ 52 
Figure 4-36 My_EnumerationImplType_CompuMethod ................................ ............... 52 
Figure 4-37 My_EnumerationImplType_CompuMethod text table ................................ 53 
Figure 4-38 My_EnumerationImplInterface ................................ ................................ .. 53 
Figure 4-39 New mode declaration group ................................ ................................ .... 55 
Figure 4-40 My_ModeDeclarationGroup ................................ ................................ ...... 56 
Figure 4-41 My ModePortInterface ................................ ................................ .............. 56 
Figure 4-42 Mode ports connection ................................ ................................ ............. 57 
Figure 4-43 Mode port access ................................ ................................ ..........

### Page 6

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
6 / 80 
1 Introduction 
This technical reference aims at presenting Data Type modeling with Vector DaVinci tool 
chain in Autosar 4.0.3 context.

### Page 7

Technical Reference Autosar 4.0 - DataTypes 
2014, Vector Informatik GmbH Version: 1.1 
based on template version 5.1.0 
7 / 80 
2 Data Types and Data Prototypes 
Embedded software uses data elements , which are entities containing information 
computed by algorithms, carried between application blocks, used as reference value, etc. 
Data elements are designed according to the information they need to represent. The 
structure definition of a data element is called data type. 
In Autosar specification (see [1]) data elements are called data prototypes because they 
are the prototype or the instance of a certain data type that they re ference. Data 
prototypes can be variable elements of a sender/receiver port interface, operation 
arguments of a client/server interface, modes of a mode switch interface, calibration 
parameters, per instance memory parameters, inter-runnable variables, etc. 
Data prototypes may have different levels of representation. They may have a physical 
meaning, like speed information, or temperature information. They also must have an 
internal meaning which is used at code level, like 8 bit integer, or Boolean. 
In order to carry these di

*Excerpt: first 8 of 80 pages shown.*
