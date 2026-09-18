---
title: '_Bmw_5441_Eps_Impl_A — ProductInformation_2_MSR4-MICROSARSafe'
description: 'Converted PDF document ProductInformation_2_MSR4-MICROSARSafe.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `ProductInformation_2_MSR4-MICROSARSafe.pdf` (PDF, 1228 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 68; title: MICROSAR Safe; author: Jonas Wolf

## Converted content

### Page 1

MICROSAR Safe 
Product Information 
 
 
Version 1.9.1 
 
 
 
 
 
 
 
 
 
 
 
Authors Jonas Wolf 
Status Released

### Page 2

Product Information MICROSAR Safe 
© 2017 Vector Informatik GmbH Version 1.9.1 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Jonas Wolf 2015-10-31 1.0.0 Initial creation. 
Jonas Wolf 2015-11-13 1.0.1 Remove GPT safety feature, add COM 
constraints 
Jonas Wolf 2015-11-26 1.0.2 Adapt release types 
Jonas Wolf 2015-12-01 1.0.3 Review of TSRs finished 
Jonas Wolf 2015-12-10 1.0.4 Review comments by visrn 
Jonas Wolf 2015-12-17 1.0.5 Safety manager mail contact details 
changed 
Jonas Wolf 2016-01-19 1.1.0 Review by vismoe; Partitioning details 
added. 
Jonas Wolf 2016-01-19 1.1.1 Fix term for SafeWDG 
Jonas Wolf 2016-01-26 1.1.2 Fix typos 
Jonas Wolf 2016-01-29 1.1.3 Update information from safety manual 
Jonas Wolf 2016-03-08 1.2.0 Update information from safety manual 
Update roadmap 
Update Safety Case delivery 
Update of format 
Update delivery process 
Jonas Wolf 2016-06-28 1.2.1 Update of lead time for production delivery 
Jonas Wolf 2016-08-08 1.3.0 Update of roadmap 
Jonas Wolf 2016-08-08 1.3.1 Remove constraint of PDUR 
Jonas Wolf 2016-09-05 1.3.2 Update of roadmap 
Jonas Wolf 2016-10-26 1.4.0 Update on XCP and AMD cluster 
Update on Ethernet 
Update on lead time for Safety Case for 
ASIL A/B 
Update of document structure 
Jonas Wolf 2016-12-12 1.4.1 Update on Ethernet availability 
Jonas Wolf 2017-01-10 1.5.0 Availability information revised 
Moved TLS to Ethernet cluster 
Removed constraint on COM 
Jonas Wolf 2017-03-16 1.6.0 Added information that post build is not 
recommended 
Detail information on delivery dates 
Update to AUTOSAR 4.3 
Update of availability 
Rene Isau 2017-03-23 1.6.1 Corrected minor typos 
Rene Isau 2017-03-27 1.6.2 Updated delivery time for Safety Case 
Jonas Wolf 2017-06-20 1.7.0 Introduc

### Page 3

Product Information MICROSAR Safe 
© 2017 Vector Informatik GmbH Version 1.9.1 3 
based on template version 5.12.0 
Production (Safety-ready) 
Update of Technical Safety Requirements 
Jonas Wolf 2017-07-14 1.7.1 Added information on SOMEIPTP 
Jonas Wolf 2017-08-15 1.8.0 Added information on vSENT, SafeETH, 
XFs, OEM SWCs 
Update of illustrations to fix typos 
Jonas Wolf 2017-08-17 1.8.1 Added information on Safety Case 
Jonas Wolf 2017-08-18 1.9.0 Simplification of delivery process and more 
information on issue reporting 
Incorporate safety manual updates 
Jonas Wolf 2017-12-12 1.9.1 Make information about delivery process 
more precise 
Reference Documents 
No. Source Title Version 
[1] ISO ISO 26262 
Road vehicles — Functional safety 
2011/2012

### Page 4

Product Information MICROSAR Safe 
© 2017 Vector Informatik GmbH Version 1.9.1 4 
based on template version 5.12.0 
Contents 
1 Introduction................................ ................................ ................................ ................... 8 
1.1 Purpose ................................ ................................ ................................ ............. 8 
1.2 Scope ................................ ................................ ................................ ................ 8 
1.3 Overview ................................ ................................ ................................ ............ 8 
2 Safety Concept ................................ ................................ ................................ ............. 9 
2.1 Overview ................................ ................................ ................................ ............ 9 
2.2 Partitioning Options ................................ ................................ ............................ 9 
2.3 Safety Concept ................................ ................................ ................................ 10 
2.3.1 Technical Solution ................................ ................................ ............ 10 
2.3.2 Tool Confidence ................................ ................................ ............... 11 
2.4 Technical Safety Requirements ................................ ................................ ........ 12 
2.4.1 Initialization ................................ ................................ ...................... 12 
2.4.2 Self-test ................................ ................................ ............................ 12 
2.4.3 Reset of ECU ................................ ................................ ....

### Page 5

Product Information MICROSAR Safe 
© 2017 Vector Informatik GmbH Version 1.9.1 5 
based on template version 5.12.0 
3.2.3 Safety Case ................................ ................................ ..................... 27 
3.3 Prerequisites ................................ ................................ ................................ .... 28 
3.4 Prototype SIPs and Evaluation Bundles ................................ ........................... 28 
4 Components of MICROSAR Safe ................................ ................................ ............... 29 
4.1 Operating System ................................ ................................ ............................ 29 
4.2 Microcontroller Abstraction (MCAL) ................................ ................................ .. 30 
4.3 External Components (EXT) ................................ ................................ ............ 38 
4.4 System Services ................................ ................................ .............................. 41 
4.5 Crypto Services ................................ ................................ ............................... 44 
4.6 Diagnostic Services ................................ ................................ ......................... 45 
4.7 Memory Services ................................ ................................ ............................. 47 
4.8 Communication ................................ ................................ ................................ 48 
4.9 Advanced Measurement and Debug (AMD) ................................ ..................... 52 
4.10 XCP ................................ ................................ ................................ ................. 53 
4.11 CAN ................................ ....

### Page 6

Product Information MICROSAR Safe 
© 2017 Vector Informatik GmbH Version 1.9.1 6 
based on template version 5.12.0 
Illustrations 
Figure 1-1 Structure of MICROSAR Safe ................................ ................................ ..... 8 
Figure 2-1 BSW in “QM”-partition (left), BSW in “ASIL”-partition (right) ...................... 10 
Figure 3-1 Overview of delivery process for safety projects ................................ ....... 25 
 
Tables 
Table 4-1 Component OS ................................ ................................ ......................... 29 
Table 4-2 Component ADCDRV ................................ ................................ ............... 30 
Table 4-3 Component CANDRV ................................ ................................ ............... 30 
Table 4-4 Component LINDRV ................................ ................................ ................. 30 
Table 4-5 Component FRDRV ................................ ................................ .................. 31 
Table 4-6 Component ETHDRV ................................ ................................ ............... 31 
Table 4-7 Component WETHDRV ................................ ................................ ............ 31 
Table 4-8 Component ETHSWTDRV ................................ ................................ ........ 32 
Table 4-9 Component FLSDRV ................................ ................................ ................ 32 
Table 4-10 Component EEPDRV ................................ ................................ ............... 32 
Table 4-11 Component SPIDRV ..........................

*Excerpt: first 8 of 68 pages shown.*
