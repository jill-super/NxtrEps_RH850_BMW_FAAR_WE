---
title: 'WdgIf — TechnicalReference_WdgIf'
description: 'Converted PDF document TechnicalReference_WdgIf.pdf from module WdgIf.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_WdgIf.pdf` (PDF, 1413 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 47; title: MICROSAR WDGIF; author: Christian Leder, Rene Isau

## Converted content

### Page 1

MICROSAR WDGIF 
Technical Reference 
 
 
Version 1.2.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Christian Leder, Rene Isau 
Status Released

### Page 2

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Christian Leder, 
Rene Isau 
2016-03-16 1.0.0 First version of the migrated WdgIf 
Technical Reference 
Christian Leder 2016-07-13 1.1.0 Update after introduction of native CFG5 
generator 
Christian Leder 2017-01-09 1.2.0 Update after removing state combiner 
automatic mode 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_WatchdogInterface.pdf V2.3.0 
[2] Vector 
Informatik 
Safety Manual 
[3] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V1.4.0 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas t he programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 3 
based on template version 5.12.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 6 
2 Introduction................................ ................................ ................................ ................... 7 
2.1 Architecture Overview ................................ ................................ ........................ 8 
2.2 Basic Functionality of the WdgIf ................................ ................................ ....... 10 
3 Functional Description ................................ ................................ ............................... 11 
3.1 Features ................................ ................................ ................................ .......... 11 
3.1.1 Deviations ................................ ................................ ........................ 11 
3.1.2 Additions/ Extensions ................................ ................................ ....... 12 
3.2 Operation in Multi-Core Systems ................................ ................................ ..... 12 
3.2.1 Independent Watchdog Devices ................................ ....................... 13 
3.2.2 WdgIf with a State Combiner ................................ ............................ 14 
3.2.2.1 Checking the Slave Trigger Pattern ................................ 16 
3.2.2.2 Operation of the State Combiner................................ .... 17 
3.2.2.2.1 Synchronous Mode ................................ .... 17 
3.2.2.2.2 Asynchronous Mode ................................ .. 19 
3.2.2.3 Worst Case Delay ................................ .......................... 21 
3.2.2.

### Page 4

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 4 
based on template version 5.12.0 
4.1.1 Static Files ................................ ................................ ....................... 33 
4.1.2 Dynamic Files ................................ ................................ .................. 33 
5 API Description ................................ ................................ ................................ ........... 34 
5.1 Type Definitions ................................ ................................ ............................... 34 
5.2 State Combiner Type Definitions ................................ ................................ ...... 35 
5.3 Services provided by WdgIf ................................ ................................ ............. 38 
5.3.1 WdgIf_SetMode ................................ ................................ ............... 38 
5.3.2 WdgIf_SetTriggerCondition ................................ .............................. 38 
5.3.3 WdgIf_SetTriggerWindow ................................ ................................ 39 
5.3.4 WdgIf_GetVersionInfo ................................ ................................ ...... 39 
5.4 Services used by WdgIf ................................ ................................ ................... 40 
6 Configuration ................................ ................................ ................................ .............. 42 
6.1 Configuration Variants ................................ ................................ ...................... 42 
6.2 Integration with MICROSAR / fully AUTOSAR compliant Wdg drivers .............. 42 
6.3 Configuring the State Combiner ................................ ................................ ....... 4

### Page 5

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 5 
based on template version 5.12.0 
Illustrations 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ......................... 8 
Figure 2-2 Watchdog Manager Stack in an AUTOSAR environment ............................ 9 
Figure 2-3 Layered structure of the Watchdog Interface ................................ ............ 10 
Figure 3-1 WdgM Stack on a multi-core system using WdgIf to address 
independent watchdogs for each core ................................ ...................... 13 
Figure 3-2 WdgM Stack on a multi-core system using the State Combiner for a 
combined core reaction ................................ ................................ ............ 14 
Figure 3-3 Master and slave run synchronously with a sufficient offset to avoid jitter 
effects (example 1) ................................ ................................ ................... 18 
Figure 3-4 Master and slave run synchronously with a sufficient offset (example 2)... 18 
Figure 3-5 Master and slave run synchronously with a sufficient offset (example 3)... 19 
Figure 3-6 Master and slave drifting apart although they have the same configured 
period (Pm = Ps) ................................ ................................ ........................ 20 
Figure 3-7 Master and slave do not drift from each other but jitter effects occur......... 21 
Figure 3-8 Slave skipping one trigger is not necessarily detected by master in 
asynchronous mode ................................ ................................ ................. 21 
Figure 3-9 Worst case delay of the State Combiner ................................ ................... 23 
Figure 3-10 Worst case evaluation Case 2 ..............

### Page 6

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 6 
based on template version 5.12.0 
1 Component History 
The component history gives an overview over the important milestones that are 
supported in the different versions of the component. 
Component Version New Features 
1.00 Migration of the WdgIf to Vector Informatik GmbH 
2.00 Introduction of native CFG5 generator 
2.01 Removing manual state combine mode 
Table 1-1 Component history

### Page 7

Technical Reference MICROSAR WDGIF 
© 2017 Vector Informatik GmbH Version 1.2.0 7 
based on template version 5.12.0 
2 Introduction 
This document describes the functionality, API and configuration of the AUTOSAR BSW 
module WdgIf as specified in [1]. 
 
Supported AUTOSAR Release*: 4.0.1 
Supported Configuration Variants: pre-compile 
Vendor ID: WDGIF_VENDOR_ID 30 decimal 
(= Vector-Informatik, 
according to HIS) 
Module ID: WDGIF_MODULE_ID 43 decimal 
(according to ref. [3]) 
* For the detailed functional specification please also refer to the corresponding AUTOSAR SWS. 
 
This user manual describes the Watchdog Interface (WdgIf), which is part of the Watchdog 
Manager Stack, which is part of the AUTOSAR ECU Abstraction Layer. The main WdgIf 
functionality consists of linking one or more Watchdog drivers (Wdg) to the overlying 
Watchdog Manager module (WdgM). 
For multi -core systems, the W

*Excerpt: first 8 of 47 pages shown.*
