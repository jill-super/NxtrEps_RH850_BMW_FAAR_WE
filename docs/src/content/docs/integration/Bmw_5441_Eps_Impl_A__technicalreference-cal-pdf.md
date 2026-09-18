---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Cal'
description: 'Converted PDF document TechnicalReference_Cal.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Cal.pdf` (PDF, 871 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 49; title: MICROSAR Crypto Abstraction Library; author: Wladimir Gerber, Markus Schneider

## Converted content

### Page 1

MICROSAR Crypto Abstraction Library 
Technical Reference 
 
 
Version 2.2 
 
 
 
 
 
 
 
 
 
 
 
Authors Wladimir Gerber, Markus Schneider 
Status Released

### Page 2

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
2 / 49 
Document Information 
History 
Author Date Version Remarks 
Wladimir Gerber 2012-10-01 1.0 Initial version 
Markus Schneider 2013-04-03 2.0 Updated for AUTOSAR 4; 
Adapting chapter 3.1.3, 5 and chapter 7.1 
Markus Schneider 2013-10-14 2.1 Update of chapter ‘5 Configuration’ 
Markus Schneider 2014-10-15 2.2 Added SymEncrypt, KeyDerive and 
KeyExchange services; Removed chapter 
“Component History” 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_CryptoAbstractionLibrary.pdf V1.2.0 
R4.0 
Rev 3 
[2] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V1.6.0 
R4.0 
Rev 3 
 
Scope of the Document 
This technical reference describes the general use of the Microsar Crypto Abstraction 
Library (CAL) software.

### Page 3

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
3 / 49 
Contents 
1 Introduction................................ ................................ ................................ ................... 8 
1.1 Architecture Overview ................................ ................................ ........................ 9 
2 Functional Description ................................ ................................ ............................... 11 
2.1 Features ................................ ................................ ................................ .......... 11 
2.2 Initialization ................................ ................................ ................................ ...... 12 
2.3 States ................................ ................................ ................................ .............. 12 
2.3.1 Streaming Approach................................ ................................ ......... 13 
2.4 Error Handling ................................ ................................ ................................ .. 13 
2.4.1 Development Error Reporting ................................ ........................... 13 
2.4.2 Production Code Error Reporting ................................ ..................... 13 
3 Integration ................................ ................................ ................................ ................... 14 
3.1 Scope of Delivery ................................ ................................ ............................. 14 
3.1.1 Static Files ................................ ................................ ....................... 14 
3.1.2 Dynamic Files ................................ ..............................

### Page 4

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
4 / 49 
4.2.18 Cal_SignatureVerifyStart ................................ ................................ .. 30 
4.2.19 Cal_SignatureVerifyUpdate ................................ .............................. 31 
4.2.20 Cal_SignatureVerifyFinish ................................ ................................ 32 
4.2.21 Cal_HashStart ................................ ................................ .................. 32 
4.2.22 Cal_HashUpdate ................................ ................................ .............. 33 
4.2.23 Cal_HashFinish ................................ ................................ ................ 33 
4.2.24 Cal_SymKeyExtractStart ................................ ................................ .. 34 
4.2.25 Cal_SymKeyExtractUpdate ................................ .............................. 35 
4.2.26 Cal_SymKeyExtractFinish ................................ ................................ 35 
4.2.27 Cal_SymBlockEncryptStart ................................ .............................. 36 
4.2.28 Cal_SymBlockEncryptUpdate ................................ .......................... 37 
4.2.29 Cal_SymBlockEncryptFinish ................................ ............................ 37 
4.2.30 Cal_SymBlockDecryptStart ................................ .............................. 38 
4.2.31 Cal_SymBlockDecryptUpdate ................................ .......................... 39 
4.2.32 Cal_SymBlockDecryptFinish ................................ ............................ 39 
4.2.33 Cal_MacGenerateStart ................................ ................................ .... 40 
4.2.34 Cal_MacGenerateUpd

### Page 5

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
5 / 49 
8 Contact ................................ ................................ ................................ ........................ 49

### Page 6

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
6 / 49 
Illustrations 
Figure 1-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 9 
Figure 1-2 Interfaces to adjacent modules of the CAL ................................ ............... 10 
Figure 2-1 Sequence Diagram ................................ ................................ ................... 12 
Figure 3-1 Include structure of the MSR CAL ................................ ............................. 16 
 
Tables 
Table 2-1 Supported AUTOSAR standard conform features ................................ ..... 11 
Table 2-2 Not supported AUTOSAR standard conform features ............................... 11 
Table 2-3 Features provided beyond the AUTOSAR standard ................................ .. 11 
Table 3-1 Static files ................................ ................................ ................................ . 15 
Table 3-2 Dynamic files ................................ ................................ ............................ 15 
Table 3-3 Compiler abstraction and memory mapping ................................ .............. 17 
Table 4-1 Type definitions ................................ ................................ ......................... 18 
Table 4-2 Cal_<Service>ConfigType ................................ ................................ ........ 18 
Table 4-3 Cal_<Primitive>ConfigType ................................ ................................ ...... 19 
Table 4-4 Cal_SymDecryptStart ................................ ................................ ............... 20 
Table 4-5 Cal_SymDecryptUpdate ................................ ......................

### Page 7

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on template version 5.2.0 
7 / 49 
Table 4-39 Cal_MacVerifyStart ................................ ................................ ................... 42 
Table 4-40 Cal_MacVerifyUpdate ................................ ................................ ............... 43 
Table 4-41 Cal_MacVerifyFinish ................................ ................................ ................. 43 
Table 4-42 Services used by the CAL................................ ................................ ......... 44 
Table 5-1 Common Properties ................................ ................................ .................. 45 
Table 5-2 Service Type related Properties ................................ ................................ 45 
Table 5-3 Service specific Properties ................................ ................................ ........ 46 
Table 7-1 Abbreviations ................................ ................................ ............................ 48

### Page 8

Technical Reference MICROSAR Crypto Abstraction Library 
2014, Vector Informatik GmbH Version: 2.2 
based on templa

*Excerpt: first 8 of 49 pages shown.*
