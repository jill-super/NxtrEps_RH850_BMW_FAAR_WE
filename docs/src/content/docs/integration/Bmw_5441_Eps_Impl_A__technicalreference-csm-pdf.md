---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Csm'
description: 'Converted PDF document TechnicalReference_Csm.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Csm.pdf` (PDF, 986 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 42; title: MICROSAR CSM; author: Markus Schneider, Anant Gupta

## Converted content

### Page 1

MICROSAR CSM 
Technical Reference 
 
Cryptographic Service Manager 
Version 1.03.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Markus Schneider, Anant Gupta 
Status Released

### Page 2

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Schneider, Markus 2017-03-14 1.01.00 Initial Creation for ASR 4.3 
Gupta, Anant 2017-03-17 1.01.00 Add configurational details 
Schneider, Markus 2017-05-08 1.02.00 3.1.1 Added backward compatible static 
definition limitation 
5 Adapted to Specification 
Schneider, Markus 2017-06-07 1.03.00 Adapted chapter 4.2 
Added information about SecureCounter 
Removed API description for 
SecureCounter 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_CryptoServiceManager.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf 4.3.0

### Page 3

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 3 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 7 
2 Introduction................................ ................................ ................................ ................... 8 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ............................... 10 
3.1 Features ................................ ................................ ................................ .......... 10 
3.1.1 Deviations ................................ ................................ ........................ 10 
3.2 Initialization ................................ ................................ ................................ ...... 10 
3.3 Main Functions ................................ ................................ ................................ 10 
3.4 Error Handling ................................ ................................ ................................ .. 11 
3.4.1 Development Error Reporting ................................ ........................... 11 
4 Integration ................................ ................................ ................................ ................... 13 
4.1 Scope of Delivery ................................ ................................ ............................. 13 
4.1.1 Static Files ................................ ................................ ....................... 13 
4.1.2 Dynamic Files ................................ .......................

### Page 4

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 4 
based on template version 6.0.1 
5.2.18 Csm_MacGenerate ................................ ................................ .......... 26 
5.2.19 Csm_MacVerify ................................ ................................ ................ 26 
5.2.20 Csm_Encrypt ................................ ................................ ................... 27 
5.2.21 Csm_Decrypt ................................ ................................ ................... 28 
5.2.22 Csm_AEADEncrypt ................................ ................................ .......... 29 
5.2.23 Csm_AEADDecrypt................................ ................................ .......... 30 
5.2.24 Csm_SignatureGenerate ................................ ................................ . 31 
5.2.25 Csm_SignatureVerify ................................ ................................ ....... 32 
5.2.26 Csm_RandomGenerate ................................ ................................ ... 33 
5.3 Services used by CSM ................................ ................................ ..................... 33 
5.4 Callback Functions ................................ ................................ ........................... 34 
5.4.1 Csm_CallbackNotification ................................ ................................ 34 
5.5 Service Ports ................................ ................................ ................................ ... 34 
5.5.1 Client Server Interface ................................ ................................ ..... 34 
5.5.1.1 Provide Ports on CSM Side ................................ ........... 34 
6 Configuration ................................ ................................ ......

### Page 5

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 5 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR 4.3 Architecture Overview ................................ ......................... 8 
Figure 2-2 Interfaces to adjacent modules of the CSM ................................ ................ 9 
Figure 6-1 Structural overview and basic workflow ................................ .................... 35 
Figure 6-2 Configuration CsmPrimitive ................................ ................................ ...... 36 
Figure 6-3 Configuration CryptoPrimitive ................................ ................................ ... 37 
Figure 6-4 Configuration CryptoDriverObject ................................ ............................. 37 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 7 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 10 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 10 
Table 3-3 Service IDs ................................ ................................ ............................... 12 
Table 3-4 Errors reported to DET ................................ ................................ ............. 12 
Table 4-1 Static files ................................ ................................ ................................ . 13 
Table 4-2 Generated files ................................ ................................ ......................... 13 
Table 5-1 Type definitions ................................ ................................ ......................... 14 
Table 5-2 Csm_Init ................................ .....................

### Page 6

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 6 
based on template version 6.0.1 
Table 7-1 Glossary ................................ ................................ ................................ ... 41 
Table 7-2 Abbreviations ................................ ................................ ............................ 41

### Page 7

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 7 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00 Initial beta release 
1.01 Adaptions to the specification; several improvements and bugfixes 
1.02 Serial Production Release 
1.03 SafeBsw Release 
Table 1-1 Component history

### Page 8

Technical Reference MICROSAR CSM 
© 2017 Vector Informatik GmbH Version 1.03.00 8 
based on template version 6.0.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module CSM as specified in [1]. 
 
Supported AUTOSAR Release*: 4.3 
Supported Configuration Variants: pre-compile 
Vendor ID: CSM_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: CSM_MODULE_ID 110 decimal 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The CSM provides synchronous and asynchronous services to enable a unique access to 
basic cryptographic functionalities for software components (SWC) and basic software 
(BSW). The CSM offers a standardized interface t

*Excerpt: first 8 of 42 pages shown.*
