---
title: 'Det — TechnicalReference_Det'
description: 'Converted PDF document TechnicalReference_Det.pdf from module Det.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Det.pdf` (PDF, 877 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 32; title: MICROSAR [BSW module]; author: Hartmut Hörner

## Converted content

### Page 1

MICROSAR DET 
Technical Reference 
 
 
Version 10.0.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Hartmut Hörner 
Status Released

### Page 2

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Hartmut Hörner 2007-11-29 1.0 Initial version 
Hartmut Hörner 2008-01-03 1.1 Update to AUTOSAR 3 
Hartmut Hörner 2008-04-14 1.2 Naming changed to AUTOSAR short 
name, screen shots updated. 
(ESCAN00025687) 
Hartmut Hörner 2008-09-16 1.3 Added DET extension mechanism based 
on callout. 
Added chapter 4.4. 
Hartmut Hörner 2010-01-13 2.0 Update to AUTOSAR 4 
Hartmut Hörner 2012-04-20 2.1 Added usage hints related to silent BSW 
concept in 4.7. 
(ESCAN00058419) 
Hartmut Hörner 2013-04-09 2.2 Added Configurator 5 and service port 
interface 
(ESCAN00066511) 
Hartmut Hörner 2013-09-13 2.3 Added DLT forwarding support for 
Configurator 5 
(ESCAN00068394, ESCAN00069807) 
Hartmut Hörner 2014-12-10 2.3.1 Added description of 
BCD-coded return value of 
Det_GetVersionInfo() 
(ESCAN00079310) 
Hartmut Hörner 2015-06-12 2.4.0 File name changed 
(ESCAN00081049) 
Added chapter 4.2. 
Hartmut Hörner 2016-12-24 10.0.0 Update to AUTOSAR 4.3 (FEAT-1939) 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_DET.pdf 4.3.0 
[2] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf V1.0.0

### Page 3

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 3 
based on template version 6.0.1 
Scope of the Document 
This technical reference describes the general use of the MICROSAR Default Error Tracer 
(DET). 
Note that this release of the DET supports only AUTOSAR 4 and the configuration tool 
Configurator 5. If you need a DET module for previous AUTOSAR versions or tools an 
older version is required. 
 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 4 
based on template version 6.0.1 
Contents 
1 Component History ................................ ................................ ................................ ...... 7 
2 Introduction................................ ................................ ................................ ................... 8 
2.1 Architecture Overview ................................ ................................ ........................ 8 
3 Functional Description ................................ ................................ ............................... 10 
3.1 Features ................................ ................................ ................................ .......... 10 
3.1.1 Deviations ................................ ................................ ........................ 10 
3.1.2 Additions/ Extensions ................................ ................................ ....... 10 
3.1.3 Limitations ................................ ................................ ........................ 11 
3.2 Initialization ................................ ................................ ................................ ...... 11 
3.3 States ................................ ................................ ................................ .............. 11 
3.4 Main Functions ................................ ................................ ................................ 11 
3.5 Error Handling ................................ ................................ ................................ .. 11 
3.5.1 Development Error Reporting ................................ ........................... 11 
3.5.2 Production Code Error Reporting ................................ ..................... 12 
3.6 

### Page 5

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 5 
based on template version 6.0.1 
5.2 Services provided by DET ................................ ................................ ................ 21 
5.2.1 Det_Init ................................ ................................ ............................ 21 
5.2.2 Det_InitMemory ................................ ................................ ................ 22 
5.2.3 Det_Start ................................ ................................ .......................... 22 
5.2.4 Det_GetVersionInfo ................................ ................................ .......... 23 
5.2.5 Det_ReportError ................................ ................................ ............... 23 
5.2.6 Det_ReportRuntimeError ................................ ................................ . 24 
5.2.7 Det_ReportTransientFault ................................ ................................ 25 
5.3 Services used by DET ................................ ................................ ..................... 26 
5.4 Callback Functions ................................ ................................ ........................... 26 
5.5 Configurable Interfaces ................................ ................................ .................... 26 
5.5.1 Callout Functions ................................ ................................ ............. 26 
5.5.1.1 <DetErrorHook> ................................ ............................. 26 
5.5.1.2 <DetReportRuntimeErrorCallout> ................................ .. 27 
5.5.1.3 <DetReportTransientFaultCallout> ................................ . 27 
5.6 Service Ports ................................ ................................ ....................

### Page 6

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 6 
based on template version 6.0.1 
Illustrations 
Figure 2-1 AUTOSAR 4.3 Architecture Overview ................................ ......................... 8 
Figure 2-2 Interfaces to adjacent modules of the DET ................................ ................. 9 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 7 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 10 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 10 
Table 3-3 Features provided beyond the AUTOSAR standard ................................ .. 10 
Table 3-4 Service IDs ................................ ................................ ............................... 11 
Table 3-5 Errors reported to DET ................................ ................................ ............. 12 
Table 4-1 Static files ................................ ................................ ................................ . 18 
Table 4-2 Generated files ................................ ................................ ......................... 18 
Table 5-1 Type definitions ................................ ................................ ......................... 21 
Table 5-2 Det_Init ................................ ................................ ................................ ..... 22 
Table 5-3 Det_InitMemory ................................ ................................ ........................ 22 
Table 5-4 Det_Start ................................ ................................ ................................ .. 23 
Table 5-5 Det_GetVersionInfo .......................

### Page 7

Technical Reference MICROSAR DET 
© 2017 Vector Informatik GmbH Version 10.0.0 7 
based on template version 6.0.1 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
0.01.00 Creation 
2.00.00 Updat

*Excerpt: first 8 of 32 pages shown.*
