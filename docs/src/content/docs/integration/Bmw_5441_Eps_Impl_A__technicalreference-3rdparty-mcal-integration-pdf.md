---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_3rdParty-MCAL-Integration'
description: 'Converted PDF document TechnicalReference_3rdParty-MCAL-Integration.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_3rdParty-MCAL-Integration.pdf` (PDF, 708 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 31; title: MCAL Integration Package; author: Andrej Gazvoda, Günther Piehler, Roland Süß, Ingo Wuttke

## Converted content

### Page 1

MCAL Integration Package 
Technical Reference 
 
Basics and workflows 
Version 1.04.00 
 
 
 
 
 
 
 
 
 
 
Authors Andrej Gazvoda, Günther Piehler, Roland Süß, Ingo 
Wuttke 
Status Released

### Page 2

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 2 
based on template version 5.2.0 
Document Information 
History 
Author Date Version Remarks 
Roland Süß ; Ingo Wuttke 2015-02-27 1.00.00 Initial Ideas, usage as 
Application Note; Porting to 
Technical Reference 
template; adding detailed 
description about 3rd party 
tools etc. 
Günther Piehler 2015-04-24 1.00.01 Review; small changes to 
increase understandability; 
Known Issue for missing 
config items added  
released 
Andrej Gazvoda; Roland Süß 2015-06-30 1.00.02 7.3 / 7.4 - Added known 
issues regarding EB tresos™ 
tool 
Günther Piehler 2015-07-17 1.01.00 2.3 - Introduction of Mixed 
AUTOSAR use case 
3 ff - Extend description of 
MCAL preparation 
(prerequisites) 
4 - hint about recommended 
workflow added 
Günther Piehler 2015-10-26 1.01.01 3.2.2 / 3.2.3 - parameter 
corrected 
4 – added hint for MCAL 
Integration video 
Günther Piehler 2016-01-26 1.02.00 4.2 - added hint for “round 
trip” ability 
general - new CI applied 
Günther Piehler 2016-07-05 1.03.00 Page 3 - Added further useful 
documents as reference 
 
Günther Piehler 2016-09-27 1.04.00 1 – completely new 
Reference to QuickStart 
document deleted (replaced 
within this document); 
Reference to ScreenCase 
and ReleaseNote added 
Hints for AUTOSAR3 <-> 
AUTOSAR4 differentiation 
added 
3.2.2 – non-interactive mode 
introduced 
3.2.3 – reference to Release 
Notes added for further info

### Page 3

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 3 
based on template version 5.2.0 
6 – completely new 
7 – issue for “MCAL and SIP 
storage location” removed 
8 – hint to “generate all” 
added 
Reference Documents 
No. Source Title Version 
[1] Vector Product Information MICROSAR Vector SLP4 1.03.02 
[2] Vector Catalog – Product Information MICROSAR – Chapter MCAL V1.3 – 
2015-02 
[3] Vector Application Note “AN-ISC-8-1153_ThirdPartyModules.pdf” Latest 
(e.g. 1.0) 
[4] Vector Application Note “AN-ISC-8-1171_Tresos_LicenseHandling.pdf” Latest 
(e.g. 
1.00.01) 
[5] Vector Application Note “AN-ISC-8-1180_MCAL-Integration-Variants.pdf” Latest 
(e.g. 0.9) 
[6] Vector Release Note 
“ReleaseNotes_3rdPartyMCAL_VectorIntegration.pdf” 
As 
provided 
within 
your SIP 
[7] Vector ScreenCast_McalIntegration_Tresos.pdf As 
provided 
within 
your SIP 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 4

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 4 
based on template version 5.2.0 
Contents 
1 Purpose of the document ................................ ................................ ............................. 7 
2 Introduction................................ ................................ ................................ ................... 8 
2.1 Responsibility ................................ ................................ ................................ ..... 8 
2.2 Support requests................................ ................................ ................................ 9 
2.3 Mix between AUTOSAR specification versions ................................ .................. 9 
3 First Steps ................................ ................................ ................................ ................... 10 
3.1 Delivery structure ................................ ................................ ............................. 10 
3.2 Starting up ................................ ................................ ................................ ....... 11 
3.2.1 MCAL delivered within Vector SIP ................................ .................... 11 
3.2.2 MCAL not contained within Vector SIP ................................ ............. 11 
3.2.3 MCAL Update needed ................................ ................................ ...... 13 
4 Workflow ................................ ................................ ................................ ..................... 14 
4.1 Single configuration tool usage ................................ ................................ ........ 14 
4.2 Mixed configuration tool usage................................ ................................ ......... 15 
4.3 S

### Page 5

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 5 
based on template version 5.2.0 
7.4 Error messages regarding CommonPublishedInformation with EB tresos™ .... 27 
8 Frequently Asked Questions ................................ ................................ ..................... 28 
9 Glossary and Abbreviations ................................ ................................ ...................... 30 
9.1 Glossary ................................ ................................ ................................ .......... 30 
9.2 Abbreviations ................................ ................................ ................................ ... 30 
10 Contact ................................ ................................ ................................ ........................ 31

### Page 6

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 6 
based on template version 5.2.0 
Illustrations 
Figure 4-1 Configuration workflow – Mixed configuration tool usage .......................... 16 
Figure 5-1 New Configuration Project ................................ ................................ ........ 20 
Figure 5-2 Configuration Project Data ................................ ................................ ........ 21 
Figure 5-3 Component Configurations ................................ ................................ ....... 22 
Figure 5-4 Create an exporter (step 1) ................................ ................................ ....... 22 
Figure 5-5 Create an exporter (step 2 – AUTOSAR options) ................................ ...... 22 
Figure 5-6 Generate Button ................................ ................................ ....................... 23 
Figure 5-7 DEM Path using DaVinci Configurator 5 ................................ ................... 23 
Figure 5-8 Settings within DaVinci Configurator 5 Pro................................ ................ 23 
Figure 5-9 DEM-Path in the Outline window of tresos™ ................................ ............ 24 
Figure 5-10 DEM-Path within tresos™ ................................ ................................ ......... 24 
Figure 5-11 Settings for DEM within tresos™ ................................ .............................. 24 
 
Tables 
Table 4-1 Guidance for single configuration tool usage ................................ ............ 15 
Table 4-2 Guidance for mixed configuration tool mode ................................ ............. 17 
Table 4-3 Guidance for split configuration tool usage ................................ ............... 18

### Page 7

Technical Reference MCAL Integration Package 
© 2016 Vector Informatik GmbH Version 1.04.00 7 
based on template version 5.2.0 
1 Purpose of the document 
This document supports the user by launching the delivery, setting up a project and 
serving the tooling - and configuration -based interfaces between the Vector MICROSAR 
BSW and the 3rd party MCAL. 
The term “tooling” means Vector DaVinci Configurator on the one hand and a third party 
configuration and generation framework (EB tresos™, KPIT ECU Spectrum™ …) on the 
other.

### Page 8

Technical 

*Excerpt: first 8 of 31 pages shown.*
