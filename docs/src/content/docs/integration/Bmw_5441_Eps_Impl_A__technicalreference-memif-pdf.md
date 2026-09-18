---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_MemIf'
description: 'Converted PDF document TechnicalReference_MemIf.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_MemIf.pdf` (PDF, 730 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 25; title: YourTopic; author: Tobias Schmid

## Converted content

### Page 1

MICROSAR MemIf 
Technical Reference 
 
 
Version 2.02.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Tobias Schmid, Manfred Duschinger, Michael Goß 
Status Released

### Page 2

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
2 / 25 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Tobias Schmid 2008-04-14 1.0 Creation of document 
Manfred Duschinger 2013-02-20 1.01.00 Ch. 4.1. Update files 
according to new generator 
Ch. 6 Update Configuration 
Michael Goß 2014-11-21 2.01.01 Typos were corrected and 
content was modified a little 
Michael Goß 2015-04-23 2.02.00 Content was updated 
regarding SafeBSW MemIf 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_Mem_AbstractionInterface.pdf V1.4.0 
[2] AUTOSAR_SWS_DET.pdf V2.2.0 
[3] AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[4] AUTOSAR_SWS_EEPROM_Abstraction.pdf V2.0.0 
[5] AUTOSAR_SWS_Flash_EEPROM_Emulation.pdf V2.0.0 
Table 1-2 Reference documents 
 
1.3 Scope of the Document 
This technical reference describes the general use of module MemIf (AUTOSAR Memory 
Abstraction Interface). 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
3 / 25 
Contents 
1 Document Information ................................ ................................ ................................ . 2 
1.1 History ................................ ................................ ................................ ............... 2 
1.2 Reference Documents ................................ ................................ ....................... 2 
1.3 Scope of the Document................................ ................................ ...................... 2 
2 Introduction................................ ................................ ................................ ................... 6 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 8 
3.1 Features ................................ ................................ ................................ ............ 8 
3.2 Initialization ................................ ................................ ................................ ........ 8 
3.3 Main Functions ................................ ................................ ................................ .. 8 
3.4 Error Handling ................................ ................................ ................................ .... 8 
3.4.1 Development Error Reporting ................................ ............................. 8 
3.4.1.1 Parameter Checking ................................ ........................ 9 
4 Integration ................................ ................................ ...............

### Page 4

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
4 / 25 
7 AUTOSAR Standard Compliance................................ ................................ ............... 23 
7.1 Deviations ................................ ................................ ................................ ........ 23 
7.1.1 Extension of Error Codes ................................ ................................ . 23 
7.2 Additions/ Extensions ................................ ................................ ....................... 23 
8 Glossary and Abbreviations ................................ ................................ ...................... 24 
8.1 Glossary ................................ ................................ ................................ .......... 24 
8.2 Abbreviations ................................ ................................ ................................ ... 24 
9 Contact ................................ ................................ ................................ ........................ 25

### Page 5

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
5 / 25 
Illustrations 
Figure 2-1 AUTOSAR architecture ................................ ................................ ............... 7 
Figure 2-2 Interfaces to adjacent modules of the MemIf................................ ............... 7 
Figure 4-1 Include structure ................................ ................................ ....................... 12 
Figure 5-1 MemIf interactions with other BSW ................................ ........................... 14 
 
Tables 
Table 1-1 History of the document ................................ ................................ .............. 2 
Table 1-2 Reference documents ................................ ................................ ................. 2 
Table 3-1 Supported SWS features ................................ ................................ ............ 8 
Table 3-2 Mapping of service IDs to services ................................ ............................. 9 
Table 3-3 Errors reported to DET ................................ ................................ ............... 9 
Table 3-4 Development Error Reporting: Assignment of checks to services ............... 9 
Table 4-1 Static files ................................ ................................ ................................ . 11 
Table 4-2 Generated files ................................ ................................ ......................... 11 
Table 4-3 Compiler abstraction and memory mapping ................................ .............. 13 
Table 5-1 Type definitions ................................ ................................ ......................... 15 
Table 5-2 MemIf_GetVersionInfo ....................

### Page 6

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
6 / 25 
2 Introduction 
This document describes the functionality, API and configuration of the AUTO SAR BSW 
module MemIf as specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: PRE-COMPILE 
 
Vendor ID: MEMIF_VENDOR_ID 30 decimal 
(= Vector -Informatik, 
according to HIS) 
Module ID: MEMIF_MODULE_ID 22 decimal 
(according to ref. [3]) 
* For the precise AUTOSAR Release 4.x please see the release specific documentation. 
 
MemIf (Memory Abstraction Interface) provides the interface that is used by the NvM to 
access NV memory devices. Two different types of NV memory are intended for use: Flash 
memory and EEPROM. To abstract the hardware dependencies of the memory devices, 
low level drivers with a commonly defined API are used: Fls and Eep (internal or external). 
These modules are abstracted by the modules Fee (Flash EEPROM Emulation) and Ea 
(EEPROM Abstraction). Both modules may exist at the same time. 
MemIf offers a common interface for accessing Fee or Ea instances. In order to distinguish 
those different instances MemIf provides a set of device handles, which may be used for 
configuration of NvM.

### Page 7

Technical Reference MICROSAR MemIf 
2015, Vector Informatik GmbH Version: 2.02.00 
based on template version 3.1 
7 / 25 
2.1 Architecture Overview 
The following figure shows where the MemIf is located in the AUTOSAR architecture. 
 
Figure 2-1 AUTOSAR architecture 
 
The next figure shows the interfaces to adjacent modules of the MemIf. These interfaces 
are described in chapter 5. 
FR 
CAN IF FR IF
COM DCM
IPDU
Fee
MemI

*Excerpt: first 8 of 25 pages shown.*
