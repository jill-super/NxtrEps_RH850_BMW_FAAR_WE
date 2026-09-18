---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_E2E'
description: 'Converted PDF document TechnicalReference_E2E.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_E2E.pdf` (PDF, 695 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 26; title: MICROSAR E2E; author: Michael Goß

## Converted content

### Page 1

MICROSAR E2E 
Technical Reference 
 
 
Version 1.02.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Michael Goß 
Status Released

### Page 2

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Michael Goß 2015-07-03 1.00.00 Initial version 
Michael Goß 2015-10-21 1.01.00 Support of JLR E2E profile 
Michael Goß 2016-11-25 1.02.00 Support of E2E profile 7 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_E2ELibrary.pdf V4.2.1 
[2] AUTOSAR AUTOSAR_SWS_E2ELibrary.pdf V4.3.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V4.2.1 
Scope of the Document 
This technical reference de scribes the general use of the E2E library basis software. The 
E2E Library was developed according to ISO 26262 for use in safety -related items. There 
are no aspects which are controller specific. 
 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 3 
based on template version 5.12.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ............................... 10 
3.1 Features ................................ ................................ ................................ .......... 10 
3.2 E2E Communication Protection ................................ ................................ ....... 10 
3.2.1 Communication Faults ................................ ................................ ..... 10 
3.2.2 Fault Model ................................ ................................ ...................... 11 
3.2.3 Protection mechanisms ................................ ................................ .... 11 
3.2.4 Detected Communication Faults ................................ ...................... 12 
3.3 Initialization ................................ ................................ ................................ ...... 12 
3.4 States ................................ ................................ ................................ .............. 12 
3.5 Main Functions ................................ ................................ ................................ 13 
3.6 Error Handling ................................ ................................ ................................ .. 13 
4 Int

### Page 4

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 4 
based on template version 5.12.0 
6 Configuration ................................ ................................ ................................ .............. 24 
7 Glossary and Abbreviations ................................ ................................ ...................... 25 
7.1 Glossary ................................ ................................ ................................ .......... 25 
7.2 Abbreviations ................................ ................................ ................................ ... 25 
8 Contact ................................ ................................ ................................ ........................ 26

### Page 5

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 5 
based on template version 5.12.0 
Illustrations 
Figure 2-1 AUTOSAR 4.2 Architecture Overview ................................ ......................... 8 
Figure 2-2 Interfaces to adjacent modules of E2E component ................................ ..... 9 
Figure 3-1 E2E State Machine ................................ ................................ ................... 13 
Figure 4-1 Include structure containing all possible E2E profiles ................................ 15 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 10 
Table 3-2 Features provided beyond the AUTOSAR standard ................................ .. 10 
Table 3-3 Provided E2E protection mechanisms ................................ ...................... 12 
Table 3-4 Detected communication faults ................................ ................................ . 12 
Table 4-1 Static files ................................ ................................ ................................ . 14 
Table 4-2 Example for setting E2E Profile 1 in E2E_cfg.mak ................................ .... 16 
Table 5-1 Type definitions ................................ ................................ ......................... 18 
Table 5-2 E2E_PXXProtect ................................ ................................ ...................... 19 
Table 5-3 E2E_PXXProtectInit ................................ ................................ .................. 19 
Table 5-4 E2E_PXXCheck ................................ ................................ ......................

### Page 6

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 6 
based on template version 5.12.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Initial creation of E2E Library documentation summarizing all supported 
E2E profiles. 
1.01.00 Documentation was updated according to additional E2E profile for JLR 
1.02.00 Documentation was updated according to additional E2E profile 7 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR E2E 
© 2017 Vector Informatik GmbH Version 1.02.00 7 
based on template version 5.12.0 
2 Introduction 
This document describes the functionality and API of the AUTOSAR BSW module E2E as 
specified in [1]. 
 
Supported AUTOSAR Release*: 4 
Supported Configuration Variants: - 
Vendor ID: E2E_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: E2E_MODULE_ID 207 decimal 
(according to ref. [3]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
 
E2E Library provides mechanisms to protect safety -related data exchange at runtime 
against the effects of faults within the communication link. 
To provide appropriate solution addressing flexibility and standardization, AUTOSAR 
specifies a set of flexible E2E profiles that implement a combination of E2E protection 
mechanisms, i.e. Profile 1, 2, 4, 5 , 6 and 7 . Additionally, an E2E profile for JLR is 
supported, which is b ased on AUTOSAR Profile 1. Each specified E2E profile has a fixed 
behavior, but it has some configuration options by function parameters (e.g. the location of 
the CRC in relation to the data, which are to be protected). This document illustrates the 
functional principle of E2E without getting too deep into details about any particular E2E 
profile. For information about the used E2E profile (e.g. data layout, CRC computation) , 
refer to [1] and [2]. 
The E2E protection allows the following: 
> It protects the safety-related data elements to be sent over the RTE by attaching 
control data (E2E Header) 
> It verifies the safety-related data elements received from the RTE using the control 
data (E2E Header) 


*Excerpt: first 8 of 26 pages shown.*
