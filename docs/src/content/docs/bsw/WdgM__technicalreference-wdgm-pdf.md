---
title: 'WdgM — TechnicalReference_WdgM'
description: 'Converted PDF document TechnicalReference_WdgM.pdf from module WdgM.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_WdgM.pdf` (PDF, 2843 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 98; title: MICROSAR WDGM; author: Christian Leder, Daniel Richter

## Converted content

### Page 1

MICROSAR WDGM 
Technical Reference 
 
 
Version 1.2.1 
 
 
 
 
 
 
 
 
 
 
 
Authors Christian Leder, Daniel Richter 
Status Released

### Page 2

Technical Reference MICROSAR WDGM 
© 2017 Vector Informatik GmbH Version 1.2.1 2 
based on template version 5.12.0 
Document Information 
History 
Author Date Version Remarks 
Daniel Richter, 
Christian Leder 
2016-02-12 1.0.0 First version of the migrated WdgM Technical 
Reference 
Christian Leder 2016-07-13 1.1.0 Update after introduction of native CFG5 generator 
Christian Leder 2017-03-01 1.2.0 Mode Port functionality added 
Timebase source OsCounter added 
Christian Leder 2017-07-25 1.2.1 Hint about initialization within a safety-related 
system added in 3.2 Initialization 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_WatchdogManager.pdf V2.0.0 
[2] AUTOSAR AUTOSAR_SWS_WatchdogInterface.pdf V2.3.0 
[3] AUTOSAR AUTOSAR_SWS_WatchdogDriver.pdf V2.3.0 
[4] Vector 
Informatik 
TechnicalReference_WdgIf.pdf V1.0.0 
[5] Vector 
Informatik 
Safety Manual 
[6] ISO Road vehicles – Functional safety ISO 
26262-
1:2011(E) 
[7] AUTOSAR AUTOSAR_TR_BSWModuleList.pdf V1.4.0 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expre ssly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference MICROSAR WDGM 
© 2017 Vector Informatik GmbH Version 1.2.1 3 
based on template version 5.12.0 
Contents 
1 Component History ................................ ................................ ................................ ...... 8 
2 Introduction................................ ................................ ................................ ................... 9 
2.1 Architecture Overview ................................ ................................ ...................... 10 
2.2 Use Cases ................................ ................................ ................................ ....... 13 
2.3 Basic Functionality of the WdgM ................................ ................................ ...... 14 
2.3.1 Supervised Entity and Program Flow Supervision ............................ 14 
2.3.2 Program Flow Supervision ................................ ............................... 15 
2.3.3 Deadline Supervision ................................ ................................ ....... 16 
2.3.4 Alive Supervision ................................ ................................ ............. 20 
2.3.5 More Details on Checkpoints and Transitions................................ ... 23 
2.3.6 Global Transitions ................................ ................................ ............ 24 
2.3.7 Global Transitions and Program Flow ................................ .............. 26 
2.3.7.1 Example of an Incorrect Global Transition Split .............. 26 
2.3.7.2 Example of an Incorrect Program Split in the Middle of 
an Entity ................................ ................................ ......... 26 
2.3.8 WdgM Supervision Cycle ................................ ................................ . 27 
2.3.9 Fault Detection Time Eval

### Page 4

Technical Reference MICROSAR WDGM 
© 2017 Vector Informatik GmbH Version 1.2.1 4 
based on template version 5.12.0 
3.1.2 Additions/ Extensions ................................ ................................ ....... 50 
3.2 Initialization ................................ ................................ ................................ ...... 51 
3.3 Memory Sections ................................ ................................ ............................. 54 
3.3.1 Memory Sections Details ................................ ................................ . 55 
3.3.2 Code and Constants ................................ ................................ ........ 56 
3.3.3 Module Variables ................................ ................................ ............. 56 
3.3.3.1 Module Variables with MICROSAR Os Gen6 / 
AUTOSAR Os version 4.0 ................................ .............. 56 
3.3.3.2 Module Variables with MICROSAR Os Gen7 / 
AUTOSAR Os version 4.2 ................................ .............. 57 
3.3.4 Supervised Entity Variables ................................ .............................. 58 
3.3.4.1 Supervised Entity Variables with MICROSAR Os 
Gen6 / AUTOSAR Os version 4.0 ................................ .. 58 
3.3.4.2 Supervised Entity Variables with MICROSAR Os 
Gen7 / AUTOSAR Os version 4.2 ................................ .. 58 
3.4 Timing Setup ................................ ................................ ................................ .... 59 
3.4.1 Deadline Measurement and Tick Counter ................................ ........ 61 
3.5 Using Checkpoints in Interrupts ................................ ................................ ....... 63 
3.6 Integration into a Multi-Core System ................................ .............

### Page 5

Technical Reference MICROSAR WDGM 
© 2017 Vector Informatik GmbH Version 1.2.1 5 
based on template version 5.12.0 
5.2.9 WdgM_GetGlobalStatus ................................ ................................ .. 76 
5.2.10 WdgM_CheckpointReached ................................ ............................. 77 
5.2.11 WdgM_PerformReset ................................ ................................ ....... 77 
5.2.12 WdgM_GetFirstExpiredSEID ................................ ............................ 78 
5.2.13 WdgM_GetFirstExpiredSEViolation ................................ .................. 79 
5.2.14 WdgM_UpdateTickCount ................................ ................................ . 79 
5.3 Services used by WdgM ................................ ................................ .................. 80 
5.4 Configurable Interfaces ................................ ................................ .................... 82 
5.4.1 Notifications ................................ ................................ ..................... 82 
5.4.1.1 Global state callback ................................ ...................... 82 
5.4.1.2 Local state change notification ................................ ....... 84 
5.5 Service Ports ................................ ................................ ................................ ... 85 
5.5.1 Client Server Interface ................................ ................................ ..... 85 
5.5.1.1 Provide Ports on WdgM Side ................................ ......... 85 
5.5.1.1.1 Port Prototype for 
WdgM_AliveSupervision ............................ 85 
5.5.1.1.2 Port Prototype for WdgM_LocalStatus ....... 86 
5.5.1.1.3 Port Prototype for WdgM_General ............. 86 
5.5.1.2 Require Ports on WdgM Side ...................

### Page 6

Technical Reference MICROSAR WDGM 
© 2017 Vector Informatik GmbH Version 1.2.1 6 
based on template version 5.12.0 
Figures 
Figure 2-1 AUTOSAR 4.x Architecture Overview ................................ ...................... 10 
Figure 2-2 Watchdog Manager Stack in an AUTOSAR environment ......................... 11 
Figure 2-3 Layered structure of the Watchdog Manager ................................ ........... 12 
Figure 2-4 Example of a simple supervised entity with a control flow ........................ 15 
Figure 2-5 Example of a simple supervised entity with deadlines .............................. 17 
Figure 2-6 Example of multiple outgoing transitions with deadlines .......................... 18 
Figure 2-7 Example of a the case where only one of several outgoing transitions 
has a deadline ................................ ................................ .......................... 19 
Figure 2-8 A task being monitored during one WdgM supervision cycle (20ms) ........ 22 
Figure 2-9 A task being mon

*Excerpt: first 8 of 98 pages shown.*
