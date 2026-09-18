---
title: 'Fr — TechnicalReference_Fr_V85x'
description: 'Converted PDF document TechnicalReference_Fr_V85x.pdf from module Fr.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Fr_V85x.pdf` (PDF, 367 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 24; title: MICROSAR Fr ERay; author: Juergen Schaeffer, Mario Kunz, Sebastian Gärtner, Sebastian Schmar, Oliver Reineke, Roland Hocke, Matthias Müller

## Converted content

### Page 1

MICROSAR Fr ERay 
Technical Reference 
 
Communication Controller E-Ray V850 
Version 1.41 
 
 
 
 
 
 
 
 
 
 
 
Authors Juergen Schaeffer, Mario Kunz, Sebastian Gärtner, 
Sebastian Schmar, Oliver Reineke, Roland Hocke, 
Matthias Müller 
Status Released

### Page 2

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
2 / 24 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Roland Hocke 2013-05-14 1.34 Creation and content copy 
from MSR3 document 
 2013-06-26 1.35 Remove obsolete MTS 
Roland Hocke 2014-01-29 1.37 Buffer alignment hints 
 
Matthias Müller 2015-02-20 1.38 Renaming of document name 
Matthias Müller 2015-09-28 1.39 Description of Endinit and 
Protected Register Access 
Matthias Müller 2015-11-27 1.40 ESCAN00080370 The usage 
of the Appl_TricoreAurixInit() 
function is not described in 
the TechRef 
SafeBSW limitations 
Matthias Müller 2017-02-01 1.41 Added hint about the specifics 
of RH850 P1X 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_DevelopmentErrorTracer.pdf 3.2.0 
[2] AUTOSAR_SWS_DiagnosticEventManager.pdf 4.2.0 
[3] TechnicalReference_Fr.pdf 1.0 or later 
[4] E-Ray_Errata_Sheet_20100215.pdf and later REL20100215 and 
later 
[5] TechnicalReference_SchM.pdf 2.5 or later 
Table 1-2 Reference documents 
1.3 Scope of the Document 
 
This technical reference describes the specific use of the FlexRay ERay driver software. It 
supplements the general FlexRay driver technical reference [3].

### Page 3

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
3 / 24 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
4 / 24 
Contents 
1 Document Information ................................ ................................ ................................ ... 2 
1.1 History ................................ ................................ ................................ ............. 2 
1.2 Reference Documents ................................ ................................ ..................... 2 
1.3 Scope of the Document ................................ ................................ ................... 2 
2 Hardware Overview ................................ ................................ ................................ ........ 7 
3 Component History ................................ ................................ ................................ ........ 8 
4 Introduction ................................ ................................ ................................ .................... 9 
5 Functional Description ................................ ................................ ................................ 10 
6 Integration ................................ ................................ ................................ .................... 11 
6.1 Scope of Delivery ................................ ................................ .......................... 11 
6.1.1 Static Files ................................ ................................ ................................ ..... 11 
6.1.2 Dynamic Files................................ ................................ ................................ 11 
6.2 Compiler Abstraction and Memory Mapping ................................ .................. 11 
6.3 Critical Se

### Page 5

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
5 / 24 
7.5 Services used by Fr ERay ................................ ................................ ............. 20 
7.6 Callback Functions ................................ ................................ ........................ 20 
7.7 Configurable Interfaces ................................ ................................ ................. 20 
7.7.1 Notifications ................................ ................................ ................................ .. 20 
7.7.2 Callout Functions ................................ ................................ .......................... 20 
8 Configuration................................ ................................ ................................ ................ 21 
8.1 Hardware Fifo................................ ................................ ................................ 21 
8.2 Configuration with DaVinci Configurator 5 ................................ ..................... 21 
9 AUTOSAR Standard Compliance ................................ ................................ ................ 22 
9.1 Deviations ................................ ................................ ................................ ..... 22 
9.1.1 Fr_GetSyncFrameList ................................ ................................ ................... 22 
9.1.2 Fr_GetPOCStatus ................................ ................................ ......................... 22 
9.2 Additions/ Extensions ................................ ................................ .................... 22 
9.3 Limitations ................................ ................................ ...................

### Page 6

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
6 / 24 
Illustrations 
Es konnten keine Einträge für ein Abbildungsverzeichnis gefunden werden. 
Tables 
Table 1-1 History of the document ................................ ................................ .............. 2 
Table 1-2 Reference documents ................................ ................................ ................. 2 
Table 2-1 Supported Hardware Overview ................................ ................................ ... 7 
Table 2-2 Supported Errata ................................ ................................ ........................ 7 
Table 3-1 Component history................................ ................................ ...................... 8 
Table 6-1 Static files ................................ ................................ ................................ . 11 
Table 6-2 Compiler abstraction and memory mapping ................................ .............. 12 
Table 6-3 CC base address ................................ ................................ ...................... 14 
Table 6-4 Message RAM ................................ ................................ .......................... 15 
Table 7-1 Fr_IrqLine0/Fr_IrqLine1 ................................ ................................ ............ 18 
Table 7-2 Fr_IrqTimer0 ................................ ................................ ............................. 19 
Table 7-3 Configuration dependent services used by Fr ERay ................................ . 20 
Table 10-1 Glossary ................................ ................................ ................................ ... 23 
Table 10-2 Abbreviations ......

### Page 7

Technical Reference MICROSAR Fr ERay Communication Controller E-Ray 
2017, Vector Informatik GmbH Version: 1.41 
based on template version 3.1 
7 / 24 
2 Hardware Overview 
The following table gives you detailed information about the derivatives and compilers. As 
very important information the documentations of the hardware manufacturers are listed. 
The driver is based upon these documents in the given version. 
 
D

*Excerpt: first 8 of 24 pages shown.*
