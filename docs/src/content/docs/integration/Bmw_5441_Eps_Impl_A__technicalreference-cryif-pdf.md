---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_CryIf'
description: 'Converted PDF document TechnicalReference_CryIf.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_CryIf.pdf` (PDF, 651 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 27; title: MICROSAR CryIf; author: Markus Schneider, Philipp Ritter

## Converted content

### Page 1

MICROSAR CryIf 
Technical Reference 
 
Crypto Interface 
Version 1.2.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Markus Schneider, Philipp Ritter 
Status Released

### Page 2

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Schneider, Markus 2017-03-07 1.01.00 Initial creation of Technical Reference 
Ritter, Philipp 2017-05-08 1.02.00 Changed chapter 5.1.6, 5.1.7, 5.1.8, 5.1.11 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_CryptoInterface.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_SWS_DET.pdf 4.3.0

### Page 3

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 3 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 7 
3 Functional Description ................................ ................................ ................................ . 9 
3.1 Features ................................ ................................ ................................ ............ 9 
3.2 Initialization ................................ ................................ ................................ ........ 9 
3.3 States ................................ ................................ ................................ ................ 9 
3.4 Main Functions ................................ ................................ ................................ .. 9 
3.5 Error Handling ................................ ................................ ................................ .... 9 
3.5.1 Development Error Reporting ................................ ............................. 9 
4 Integration ................................ ................................ ................................ ................... 11 
4.1 Scope of Delivery ................................ ................................ ............................. 11 
4.1.1 Static Files ................................ ................................ ....................... 11 
4.1.2 Dynamic Files ..............................

### Page 4

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 4 
based on template version 6.0.1 
5.3.1 CryIf_CallbackNotification ................................ ................................ 23 
6 Configuration ................................ ................................ ................................ .............. 24 
6.1 Configuration Variants ................................ ................................ ...................... 24 
6.2 Configuration with DaVinci Configurator 5 Pro ................................ ................. 24 
6.2.1 General Properties ................................ ................................ ........... 24 
6.2.2 Channel Properties ................................ ................................ .......... 24 
6.2.3 Key Properties ................................ ................................ ................. 25 
7 Glossary and Abbreviations ................................ ................................ ...................... 26 
7.1 Glossary ................................ ................................ ................................ .......... 26 
7.2 Abbreviations ................................ ................................ ................................ ... 26 
8 Contact ................................ ................................ ................................ ........................ 27

### Page 5

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 5 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR 4.3 Architecture Overview ................................ ......................... 7 
Figure 2-2 Interfaces to adjacent modules of the CRYIF ................................ .............. 8 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 6 
Table 3-1 Supported AUTOSAR standard conform features ................................ ....... 9 
Table 3-2 Service IDs ................................ ................................ ............................... 10 
Table 3-3 Errors reported to DET ................................ ................................ ............. 10 
Table 4-1 Static files ................................ ................................ ................................ . 11 
Table 4-2 Generated files ................................ ................................ ......................... 11 
Table 5-1 CryIf_InitMemory ................................ ................................ ...................... 12 
Table 5-2 CryIf_Init ................................ ................................ ................................ ... 13 
Table 5-3 CryIf_GetVersionInfo ................................ ................................ ................ 13 
Table 5-4 CryIf_ProcessJob ................................ ................................ ..................... 14 
Table 5-5 CryIf_CancelJob ................................ ................................ ....................... 14 
Table 5-6 CryIf_KeyElementSet ................................ ................................ ............... 15 
Table 5-7 CryIf_K

### Page 6

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 6 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00.00 Initial beta release 
1.01.00 Adaptions to the specification; several improvements and bug fixes 
1.02.00 Release of component 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 7 
based on template version 6.0.1 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module CRYIF as specified in [1]. 
 
Supported AUTOSAR Release*: 4.3 
Supported Configuration Variants: pre-compile 
Vendor ID: CRYIF_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: CRYIF_MODULE_ID 112 decimal 
(according to ref. [1]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
 
The Crypto Interface ( CRYIF) is called by the Cryptographic Service Manager (CSM) to 
forward its service requests to the underlying Crypto Drivers (CRYPTO). The CRYIF has 
access to the CRYPTO to calculate results with their cryptographic services. These results 
are returned to the CSM by the CRYIF. 
2.1 Architecture Overview 
The following figure shows where the CRYIF is located in the AUTOSAR architecture. 
 
Figure 2-1 AUTOSAR 4.3 Architecture Overview

### Page 8

Technical Reference MICROSAR CryIf 
© 2017 Vector Informatik GmbH Version 1.2.0 8 
based on template version 6.0.1 
 
The next figure shows the interfaces to adjacent modules of the CRYIF. These interfaces 
are described in chapter 5. 
 
Figure 2-2 Interfaces to adjacent modules of the CRYIF 
 
 cmp Architecture
CRYIF
CSM
BswM Det
CRYPTO
Det_ReportError
«optional»
Cs m_<KeyManagement>
Crypto_Proces s JobCrypto_CancelJob
Cs m_<Service>
Cs m_Callback Notification
«optional»
Crypto_<KeyManagement>
CryIf_Init
CryIf_Callback Notification
«optional»
Cs m_CancelJob

*Excerpt: first 8 of 27 pages shown.*
