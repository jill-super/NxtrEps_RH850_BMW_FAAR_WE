---
title: 'IoHwAb — TechnicalReference_IoHwAb'
description: 'Converted PDF document TechnicalReference_IoHwAb.pdf from module IoHwAb.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_IoHwAb.pdf` (PDF, 1107 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 33; title: YourTopic; author: Christoph Ederer

## Converted content

### Page 1

MICROSAR IOHWAB 
Technical Reference 
 
 
Version 3.00.02 
 
 
 
 
 
 
 
 
 
 
 
Authors Christian Leder 
Status Released

### Page 2

Technical Reference MICROSAR IOHWAB 
2014, Vector Informatik GmbH Version: 3.00.02 
based on template version 5.6.0 
2 / 33 
Document Information 
History 
Author Date Version Remarks 
Christian Marchl 2007-02-09 1.00.00 Initial version 
Christian Marchl 2007-08-09 1.01.00 Typos corrected; Added description for 
component name field 
Christian Marchl 2007-12-13 1.01.01 Version adapted according to new 
version scheme 
Christoph Ederer 2008-05-21 2.00.00 Transfer of the document to new 
Technical Reference template; Adapted 
descriptions and screenshots to new 
software version 
Christoph Ederer 2008-07-11 2.00.01 Update of document due to changes in 
DCM interface and RTE usage 
Christoph Ederer 2009-01-14 2.01.00 Update of the naming of graphical 
elements in the configuration, 
Screenshots reworked, DCM 
subfunctions reworked, Added 
description of default value in 
configuration 
Christoph Ederer 2009-03-23 2.01.01 Updated development error detection 
in GUI description, toolchain naming 
updated, hints added to chapter 4.1.2 
Christoph Ederer 2009-07-21 2.02.00 Updated description of the generation 
process (user blocks, autom. SWC 
generation), updated AUTOSAR figure, 
added information on user defined 
signals 
Christoph Ederer 2009-09-25 2.02.01 Reworked description of DCM interface 
Christoph Ederer 2010-11-26 2.02.02 > Added chapter 4.3 Critical Sections 
> GUI description updated 
> Added information about necessary 
make process modifications to 4.1.2 
Christoph Ederer 2011-03-02 2.02.03 Reworked the service descriptions in 
chapters 5.4.3, 5.4.7 and 5.4.10: 
parameter ‘signal’ is [inout], now 
Christoph Ederer 2013-04-10 3.00.00 > Component rework and update to 
AUTOSAR 4 
> Update to new Configuration Tooling 
‘DaVinci Configurator 5’ 
Christian Leder 2014

### Page 3

Technical Reference MICROSAR IOHWAB 
2014, Vector Informatik GmbH Version: 3.00.02 
based on template version 5.6.0 
3 / 33 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_IOHardwareAbstraction.pdf 
(available at: 
http://www.autosar.org/download/R4.0/AUTOSAR_SWS_IOHa
rdwareAbstraction.pdf) 
V3.2.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf 
(available at: 
http://www.autosar.org/download/R4.0/AUTOSAR_SWS_Deve
lopmentErrorTracer.pdf) 
V3.2.0 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf 
(available at: 
http://www.autosar.org/download/R4.0/AUTOSAR_TR_BSWM
oduleList.pdf) 
V1.6.0 
[4] AUTOSAR AUTOSAR_EXP_VFB.pdf 
(available at: 
http://www.autosar.org/download/R4.0/AUTOSAR_EXP_VFB.
pdf) 
V2.2.0 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MICROSAR IOHWAB 
2014, Vector Informatik GmbH Version: 3.00.02 
based on template version 5.6.0 
4 / 33 
Contents 
1 Component History ................................ ................................ ................................ ...... 7 
2 Introduction................................ ................................ ................................ ................... 8 
2.1 Architecture Overview ................................ ................................ ........................ 9 
3 Functional Description ................................ ................................ ............................... 11 
3.1 Features ................................ ................................ ................................ .......... 11 
3.2 Initialization ................................ ................................ ................................ ...... 11 
3.3 States ................................ ................................ ................................ .............. 11 
3.4 Main Functions ................................ ................................ ................................ 12 
3.5 Error Handling ................................ ................................ ................................ .. 12 
3.5.1 Development Error Reporting ................................ ........................... 12 
3.5.2 Production Code Error Reporting ................................ ..................... 12 
4 Integration ................................ ................................ ................................ ................... 13 
4.1 Scope of Delivery ................................ ................................ ............................. 13 
4.1.1 Static Files ................................ .............

### Page 5

Technical Reference MICROSAR IOHWAB 
2014, Vector Informatik GmbH Version: 3.00.02 
based on template version 5.6.0 
5 / 33 
5.7 Service Ports ................................ ................................ ................................ ... 24 
5.7.1 Client Server Interface ................................ ................................ ..... 24 
5.7.1.1 Provide Ports on IOHWAB Side ................................ ..... 24 
5.7.1.1.1 Provide Ports ................................ ............. 24 
5.7.1.2 Require Ports on IOHWAB Side ................................ ..... 24 
6 Configuration ................................ ................................ ................................ .............. 25 
6.1 Configuration Variants ................................ ................................ ...................... 25 
6.2 Configuration Workflow ................................ ................................ .................... 25 
7 Glossary and Abbreviations ................................ ................................ ...................... 32 
7.1 Glossary ................................ ................................ ................................ .......... 32 
7.2 Abbreviations ................................ ................................ ................................ ... 32 
8 Contact ................................ ................................ ................................ ........................ 33

### Page 6

Technical Reference MICROSAR IOHWAB 
2014, Vector Informatik GmbH Version: 3.00.02 
based on template version 5.6.0 
6 / 33 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 9 
Figure 2-2 Interfaces to adjacent modules of the IOHWAB ................................ ........ 10 
Figure 4-1 User Block Implementation Area ................................ ............................... 15 
Figure 6-1 Configuration Workflow ................................ ................................ ............. 26 
Figure 6-2 SWC import select file ................................ ................................ .............. 27 
Figure 6-3 Imported Software Component ................................ ................................ . 28 
Figure 6-4 I/O Hardware and Application Software Component ................................ . 29 
Figure 6-5 30 
 
Tables 
Table 1-1 Component history................................ ................................ ...................... 7 
Table 3-1 Supported AUTOSAR standard conform features ................................ ..... 11 
Table 3-2 Not supported AUTOSAR standard conform features ............................... 11 
Table 3-3 Service IDs ................................ ................................ ............................... 12 
Table 3-4 Errors reported to DET ................................ ................................ ............. 12 
Table 4-1 Static files ................................ ................................ ................................ . 13 
Table 4-2 Generated fi

*Excerpt: first 8 of 33 pages shown.*
