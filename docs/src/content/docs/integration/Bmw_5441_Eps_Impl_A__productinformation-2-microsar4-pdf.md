---
title: '_Bmw_5441_Eps_Impl_A — ProductInformation_2_MICROSAR4'
description: 'Converted PDF document ProductInformation_2_MICROSAR4.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `ProductInformation_2_MICROSAR4.pdf` (PDF, 360 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 25; title: MICROSAR 4; author: Hannes Haas

## Converted content

### Page 1

MICROSAR 4 
Product Information 
 
 
Version 1.02.12 
 
 
 
 
 
 
 
 
 
 
Authors Hannes Haas 
Status Released

### Page 2

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 2 
based on template version 6.0.1 
Contents 
1 Introduction ................................ ................................ ................................ .................... 4 
2 General Information ................................ ................................ ................................ ....... 5 
2.1 Compiler Warnings ................................ ................................ ................................ ... 5 
2.2 64-bit Microcontroller Support ................................ ................................ .................. 5 
2.3 Delivery of Beta Modules/Features ................................ ................................ ........... 5 
2.4 Delivery of Stub Modules................................ ................................ .......................... 5 
2.5 Delivery of Code Templates ................................ ................................ ...................... 6 
2.6 Delivery of Example Code ................................ ................................ ........................ 6 
2.7 Usage of Features that are not Licensed ................................ ................................ .. 6 
2.8 Test Report ................................ ................................ ................................ ............... 7 
2.9 MISRA ................................ ................................ ................................ ...................... 7 
2.10 Test of External Hardware ................................ ................................ ........................ 7 
2.11 Test of 3rd Party Modules ................................ ................................ .......................... 7 
2.12 Issue Handling .........

### Page 3

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 3 
based on template version 6.0.1 
5 SIP Extensions ................................ ................................ ................................ ............. 15 
5.1 Customer Hardware ................................ ................................ ............................... 15 
5.2 Start Application ................................ ................................ ................................ ..... 15 
5.3 vVIRTUALtarget (VTT) ................................ ................................ ........................... 16 
5.3.1 Components ................................ ................................ ................................ .. 16 
5.3.2 Limitations ................................ ................................ ................................ ..... 17 
5.3.3 Required Software ................................ ................................ ........................ 18 
6 Definition of SLP/HLP/SIP , Maintenance and Release Types ................................ .... 19 
6.1 Software License Package (SLP) ................................ ................................ ........... 19 
6.2 Hardware License Package (HLP) ................................ ................................ ......... 19 
6.3 Software Integration Package (SIP) ................................ ................................ ....... 20 
6.4 Mini SIP ................................ ................................ ................................ .................. 20 
6.5 SIP Types ................................ ................................ ................................ ............... 20 
6.5.1 Beta ................................ ................................ .........

### Page 4

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 4 
based on template version 6.0.1 
1 Introduction 
All modules and options are described in the general Product Information (please refer to 
the link “Product Descriptions”). 
In addition to the general Product Information, this document provides additional details to 
the offered items.

### Page 5

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 5 
based on template version 6.0.1 
2 General Information 
 
 
Note 
This chapter provides important information that applies for using MICROSAR basic 
software. 
 
2.1 Compiler Warnings 
Due to the use of standard software modules for a huge number of different hardware 
platforms and different compilers it is not possible to avoid compiler warnings completely. 
Vector tries to keep its software free of warnings, but in some case s it is not possible or it 
may decrease performance. 
Vector provides a list of known compiler warnings with each delivery of a Production SIP. 
2.2 64-bit Microcontroller Support 
Due to limitations given by underlying specifications (ASAM, ISO, AUTOSAR…) not all 
address based services can be used on 64 -bit controllers without limitations. A typical 
limitation can be that only the lower half of the 64-bit address range can be accessed. 
2.3 Delivery of Beta Modules/Features 
Deliveries may contain Beta Modules and/or Beta Features. Beta Modules and Beta 
Features are basically operable, but not sufficiently tested, verified and/or qualified for use 
in series production and/or in vehicles operating on public or non -public roads. In 
particular, without limitation, the Beta Modules and Beta Features may cause 
unpredictable ECU behavior, may not provide all functions necessary for use in series 
production and/or may not comply with quality requirements which are necessary 
according to the state of the art. Beta Modules and Beta Features must not be used in 
series production. 
Beta Modules and Beta Features are listed in chapter 2.4 of the issue report which is 
provided with the delivery. Moreover, the issue report contains information on how to 
deactivate t

### Page 6

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 6 
based on template version 6.0.1 
and/or implementations must be tested with diligent care and must comply with all quality 
requirements which are necessary according to the state of the art before their use. 
Stub Modules can be identified by the comment section “SAMPLE CODE ONLY” in the 
implementation files. The implementation of Stub Modules can be found in 
BSW\<Msn>_Stub. Generated files are located in the generator “Source” folder using the 
naming convention <Msn>_Stub.c/h. 
2.5 Delivery of Code Templates 
The delivery may contain files that must be adapted during BSW integration. The Technical 
References of BSW modules lists the files that require to be adapted. This can be 
dedicated Template Areas or Complete Template Files (hereinafter collectively "Code 
Template"). 
Code Templates are incomplete and only intended for providing a signature and an empty 
implementation. Code Templates are neither intended nor qualified for use in series 
production without applying suitable quality measures. 
Each Code Template must be completed as described in the Technical Reference and/or in 
the respective Code Template file. The completed implementation must be tested with 
diligent care and must comply with all quality requirements which are necessary according 
to the state of the art before its use. 
2.6 Delivery of Example Code 
The delivery (SIP) may include a Start Application and/or a Demo (hereinafter collectively 
“Example Code”). The Example Code is only intended for illustrating an example of a 
possible BSW integration and BSW configuration. 
The Example Code has not passed any quality control measures and may be incomplete. 
The Example Code is neither intended nor qualified f

### Page 7

Product Information MICROSAR 4 
© 2018 Vector Informatik GmbH Version 1.02.12 7 
based on template version 6.0.1 
> the feature is not licensed for serial production purposes 
> the feature may include code that is incomplete 

*Excerpt: first 8 of 25 pages shown.*
