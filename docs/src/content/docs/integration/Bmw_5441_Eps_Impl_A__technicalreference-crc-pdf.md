---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Crc'
description: 'Converted PDF document TechnicalReference_Crc.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Crc.pdf` (PDF, 594 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 23; title: MICROSAR CRC; author: Michael Goß

## Converted content

### Page 1

MICROSAR CRC 
Technical Reference 
 
 
Version 4.03.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Michael Goß 
Status Released

### Page 2

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 2 
based on template version 5.9.0 
Document Information 
History 
Author Date Version Remarks 
Tobias Schmid 2006-12-13 1.0 Initial Version 
Tobias Schmid 2008-01-21 3.00.00 Update to ASR 2.1 
Changed versioning to new notation 
Claudia Mausz 2008-05-19 4.00.00 Update to ASR 3 
Add Crc8 calculation 
Michael Goß 2014-11-18 4.01.00 Update to ASR 4 
Add Crc8H2F calculation 
Michael Goß 2015-05-08 4.02.00 SafeBSW 
Add Crc32P4 calculation 
Michael Goß 2016-11-24 4.03.00 Add Crc64 calculation 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_CRCLibrary.pdf V4.2.0 
[2] AUTOSAR AUTOSAR_SWS_CRCLibrary.pdf V4.3.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V1.6.0 
Scope of the Document 
This technical reference describes the general use of the CRC library basis software. 
There are no aspects which are controller specific. 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 3 
based on template version 5.9.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 Features ................................ ................................ ................................ ............ 9 
3.1.1 Deviations ................................ ................................ .......................... 9 
3.1.2 Additions/ Extensions ................................ ................................ ....... 10 
3.2 Initialization ................................ ................................ ................................ ...... 10 
3.3 States ................................ ................................ ................................ .............. 10 
3.4 Main Functions ................................ ................................ ................................ 10 
3.5 Error Handling ................................ ................................ ................................ .. 10 
3.5.1 Development Error Reporting ................................ ........................... 10 
3.5.2 Production Code Error Reporting ................................ ..................... 10 
3.5.3 Parameter Checking ................................ ................................ ........ 10 
4 Integr

### Page 4

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 4 
based on template version 5.9.0 
5.6.3 Hook Functions ................................ ................................ ................ 20 
6 Configuration ................................ ................................ ................................ .............. 21 
6.1 Configuration Variants ................................ ................................ ...................... 21 
7 Glossary and Abbreviations ................................ ................................ ...................... 22 
7.1 Glossary ................................ ................................ ................................ .......... 22 
7.2 Abbreviations ................................ ................................ ................................ ... 22 
8 Contact ................................ ................................ ................................ ........................ 23

### Page 5

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 5 
based on template version 5.9.0 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 8 
Figure 4-1 Include structure ................................ ................................ ....................... 11 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 9 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 9 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 10 
Table 4-1 Static files ................................ ................................ ................................ . 11 
Table 4-2 Generated files ................................ ................................ ......................... 11 
Table 5-1 Type definitions ................................ ................................ ......................... 12 
Table 5-2 Std_VersionInfoType ................................ ................................ ................. 12 
Table 5-3 SAE-J1850 CRC8 Standard ................................ ................................ ..... 13 
Table 5-4 Crc_CalculateCRC8 ................................ ................................ ................. 13 
Table 5-5 CRC calculation based on 0x2F polynomial ................................ .............. 14 
Table 5-6 Crc_CalculateCRC8H2F ................................ ................................ ........... 14 
Table 5-7 CCITT CRC16 Standard ................................ .......................

### Page 6

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 6 
based on template version 5.9.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
4.00.00 Update to AUTOSAR Version 3 
Add Crc8 calculation 
4.01.00 Update to AUTOSAR Version 4 
Add Crc8 calculation based on 0x2F polynomial 
4.02.00 Crc32 E2E Profile 4 routine was added due to SafeBSW 
4.03.00 Crc64 (ECMA) E2E Profile 7 routine was added 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 7 
based on template version 5.9.0 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module CRC as specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: pre-compile 
Vendor ID: CRC_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: CRC_MODULE_ID 201 decimal 
(according to ref. [3]) 
* For the precise AUTOSAR Release 4.x please see the release specific documentation. 
 
 
This component implements service functions in ANSI C for calculating CRC checksums. 
The module allows pre -compile configuration of the calculation method, which is used to 
compute the CRC values. The six possible methods are table based or runtime calcula tion 
of CRC values. 
There are six different CRC calculation services available: 
> Two different services for checksum calculation of 8bit CRC value from a buffer 
> Checksum calculation of 16bit CRC value from a buffer 
> Two different services for checksum calculation of 32bit CRC value from a buffer 
> Checksum calculation of 64bit CRC value from a buffer

### Page 8

Technical Reference MICROSAR CRC 
© 2016 Vector Informatik GmbH Version 4.03.00 8 
based on template version 5.9.0 
2.1 Architecture

*Excerpt: first 8 of 23 pages shown.*
