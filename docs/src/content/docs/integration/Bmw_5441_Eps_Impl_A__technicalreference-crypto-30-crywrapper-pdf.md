---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Crypto_30_CryWrapper'
description: 'Converted PDF document TechnicalReference_Crypto_30_CryWrapper.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Crypto_30_CryWrapper.pdf` (PDF, 834 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 38; title: MICROSAR CRYPTO; author: Tobias Finke

## Converted content

### Page 1

MICROSAR CRYPTO 
Technical Reference 
 
CRYPTO CRYWRAPPER 
Version 2.1.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Tobias Finke 
Status Released

### Page 2

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Tobias Finke 2016-12-21 1.00.00 Initial creation 
Tobias Finke 2017-10-06 2.01.00 Release of component 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_CryptoDriver.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf 4.3.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 4.3.0 
[4] HIS 2009-04-01 SHE Functional Specification v1.1 (rev439) 1.1

### Page 3

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 3 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 Features ................................ ................................ ................................ ............ 9 
3.1.1 Deviations ................................ ................................ .......................... 9 
3.1.2 Additions/ Extensions ................................ ................................ ......... 9 
3.1.3 Limitations ................................ ................................ ........................ 10 
3.1.3.1 Cryptographic Algorithms and Modes ............................ 10 
3.1.3.2 Certificate Handling................................ ........................ 10 
3.1.3.3 Key Generation ................................ .............................. 10 
3.1.3.4 AEAD Det Checks ................................ ......................... 10 
3.1.3.5 Asynchronous CRY ................................ ........................ 10 
3.2 Initialization ................................ ................................ ................................ ...... 10 
3.3 Main Functions ................................ ................................ ................................ 10 
3.4 SHE Key Upda

### Page 4

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 4 
based on template version 6.0.1 
4.1 Scope of Delivery ................................ ................................ ............................. 20 
4.1.1 Static Files ................................ ................................ ....................... 20 
4.1.2 Dynamic Files ................................ ................................ .................. 20 
4.2 Critical Sections ................................ ................................ ............................... 21 
5 API Description ................................ ................................ ................................ ........... 22 
5.1 Services provided by CRYPTO ................................ ................................ ........ 22 
5.1.1 Crypto_30_CryWrapper_Init ................................ ............................. 22 
5.1.2 Crypto_30_CryWrapper_InitMemory ................................ ................ 22 
5.1.3 Crypto_30_CryWrapper_GetVersionInfo ................................ .......... 23 
5.1.4 Crypto_30_CryWrapper_ProcessJob ................................ ............... 23 
5.1.5 Crypto_30_CryWrapper_CancelJob ................................ ................. 24 
5.2 Key Management Functions ................................ ................................ ............ 25 
5.2.1 Crypto_30_CryWrapper_KeyCopy ................................ ................... 25 
5.2.2 Crypto_30_CryWrapper_KeyElementCopy ................................ ...... 25 
5.2.3 Crypto_30_CryWrapper_KeyElementIdsGet ................................ .... 26 
5.2.4 Crypto_30_CryWrapper_KeyElementSet ................................ ......... 27 
5.2.5 Crypto_30_CryWrapper_KeyValidSet ....

### Page 5

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 5 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR 4.2 Architecture Overview ................................ ......................... 7 
Figure 2-2 Interfaces to adjacent modules of the CRYPTO ................................ .......... 8 
Figure 3-1 Example SymKeyExtract Configuration for Vector CRY ............................ 18 
Figure 3-2 Example SymKeyExtract configuration for third party CRY ....................... 19 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 9 
Table 3-2 Not supported AUTOSAR standard conform features ................................ . 9 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .... 9 
Table 3-4 Service IDs ................................ ................................ ............................... 11 
Table 3-5 Errors reported to DET ................................ ................................ ............. 12 
Table 3-6 Supported data format for key import ................................ ........................ 13 
Table 3-7 Supported data format for key export ................................ ........................ 14 
Table 3-8 Overview of the required algorithm parameter ................................ .......... 15 
Table 3-9 Description of preconfigured key elements ................................ ............... 16 
Table 3-10 Description of preconfigured key types ................................ ..................... 16 
Table 3-11 Description of pre-configured keys ..........................

### Page 6

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 6 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Initial beta release 
2.00.00 Redesign of component 
2.01.00 Safe Bsw Release of Component 
Added several configurations options to support Cry implementations of 
different vendors 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 7 
based on template version 6.0.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module CRYPTO as specified in [1]. 
Supported AUTOSAR Release*: 4.3 
Supported Configuration Variants: pre-compile 
Vendor ID: CRYPTO_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: CRYPTO_MODULE_ID 114 decimal 
(according to ref. [3]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The Crypto Driver (CRYPTO) is called by the Crypto Interface (CRYIF) and performs the 
specific cryptographic functionality. The CRYPTO specification [1] offers a superset of 
algorithms which can be extended by ‘custom algorithms’. This software -based Crypto 
Driver offers a subset of algorithms and features which is described in 3.1. 
2.1 Architecture Overview 
The following figure shows where the CRYPTO is located in the AUTOSAR architecture. 
 
Figure 2-1 AUTOSAR 4.2 Architecture Overview

### Page 8

Technical Reference MICROSAR CRYPTO 
© 2017 Vector Informatik GmbH Version 2.1.0 8 
based on template version 6.0.1 
The next figure shows the interfaces to adjacent modules of the CRYPTO. These 
interfaces are described in chapt

*Excerpt: first 8 of 38 pages shown.*
