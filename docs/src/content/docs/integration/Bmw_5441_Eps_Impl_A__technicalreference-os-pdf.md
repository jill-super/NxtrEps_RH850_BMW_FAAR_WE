---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Os'
description: 'Converted PDF document TechnicalReference_Os.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Os.pdf` (PDF, 1899 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 304; title: MICROSAR OS; author: Anton Schmukel, Ivan Begert, Stefano Simoncelli, Torsten Schmidt, Da He, David Feuerstein, Michael Kock, Martin Schultheiß, Andreas Jehl, Fabian Wild, Senol Cendere, Benjamin Seifert

## Converted content

### Page 1

MICROSAR OS 
Technical Reference 
 
 
Version 2.12.0 
 
 
 
 
 
 
 
 
 
 
Authors Anton Schmukel, Ivan Begert, Stefano Simoncelli, 
Torsten Schmidt, Da He, David Feuerstein, Michael 
Kock, Martin Schultheiß, Andreas Jehl, Fabian Wild, 
Senol Cendere, Benjamin Seifert 
Status Released

### Page 2

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 2 
based on template version 6.0.1 
Document Information 
History 
Author Date Version Remarks 
Torsten Schmidt 2016-04-27 1.0.0 First release version 
Torsten Schmidt 2016-05-18 1.0.1 References to hardware manuals added. 
Revision work 
Torsten Schmidt 2016-06-03 1.0.2 Fix of ESCAN00089598 
Torsten Schmidt 2016-06-20 1.1.0 List of OS internal objects added. 
Additional startup concept chapter added. 
Chapter “Memory mapping concept” reworked. 
Description of “generate callout stubs” feature 
added. 
Torsten Schmidt 2016-07-05 1.1.1 Chapter “Memory Mapping Concept” extended. 
IOC notification callback concept changed. 
HSI of RH850 family added. 
HSI of Power PC family added. 
Torsten Schmidt 2016-07-19 1.1.2 Chapter “Memory Mapping Concept” changed. 
Hints for shorter compile times added. 
Nesting behavior of OS hooks described. 
Ivan Begert 2016-08-11 1.1.3 HSI of ARM family added. 
Torsten Schmidt 2016-08-12 1.1.4 Chapter “Memory Mapping Concept” extended. 
Chapter “Clear Pending Interrupt” extended. 
Chapter “RH850 Special Characteristics” extended. 
Ivan Begert 2016-08-18 1.1.5 HSI of ARM Zynq UltraScale added. 
Torsten Schmidt 2016-08-30 1.1.6 HSI of RH850 extended. 
Torsten Schmidt 2016-08-31 1.1.7 ORTI Debugging added. 
Timing Hook Macros reworked. 
Chapter “Memory Mapping Concept” changed. 
Chapter “Category 1 Interrupts” extended. 
Stefano Simoncelli 
Torsten Schmidt 
2016-09-15 1.1.8 Chapter “Interrupt Source API” extended. 
HSI chapter for ARM extended 
Torsten Schmidt 2016-09-22 1.2.0 VTT OS and Dual Target Concept added. 
Chapter ORTI Debugging extended. 
Anton Schmukel 
Da He 
2016-10-14 1.3.0 Ristrictions concerning API usage before StartOS() 
documented. 
Clarification concer

### Page 3

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 3 
based on template version 6.0.1 
extended. 
Correction of startup examples. 
Chapter “User include files” added. 
RH850 HSI extended. 
PPC HSI extended. 
Hardware Overview extended by RH850. 
David Feuerstein 2016-11-03 1.4.0 PPC HSI extended. 
Chapter ORTI Debugging extended. 
Michael Kock 2016-11-25 1.5.0 Updated chapter Timing Hooks 
Martin Schultheiß 2016-12-08 1.6.0 PPC HSI extended. 
Updated characteristics of VTT OS. 
David Feuerstein 
Andreas Jehl 
Ivan Begert 
Stefano Simoncelli 
2016-12-22 1.7.0 Updated precautions in PreStartTask. 
Support new Power PC Derivative: PC580003 
Support IAR compiler for ARM 
ARM Cortex-A HSI added 
David Feuerstein 
Torsten Schmidt 
2017-01-23 1.8.0 Chapter “Memory Mapping Concept” changed. 
Chapter “Resulting sections” extended. 
Chapter “X-Signals” extended. 
Chapter “API Description” extended. 
Torsten Schmidt 
Stefano Simoncelli 
David Feuerstein 
2017-02-06 
 
2.0.0 Chapter “Memory Mapping Concept” corrected. 
Chapter “MICROSAR OS Deviations from 
AUTOSAR OS Specification” extended. 
Chapter “IOC” extended. 
Feature “Fast Trusted Functions” added. 
Chapter “Non-Trusted Functions (NTF)” changed. 
ARM Cortex-M Hardware overview updated. 
Feature “Barriers” added. 
Martin Schultheiß 
Benjamin Seifert 
Da He 
Torsten Schmidt 
Stefano Simoncelli 
Anton Schmukel 
2017-03-22 2.1.0 Updated Hardware Overview for Power PC 
derivative groups (RM revisions). 
Chapter “MICROSAR OS Deviations from 
AUTOSAR OS Specification” corrected. 
Added API 
OSError_GetScheduleTableStatus_ScheduleStatus 
Chapter “ARM Special characteristic” extended. 
Chapter “Cortex-R derivatives” extended. 
Chapter “Idle Task” extended. 
TI Compiler added as supported compiler for ARM. 

### Page 4

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 4 
based on template version 6.0.1 
Martin Schultheiß 
Da He 
Extended chapter “Memory Mapping Concept”. 
Added chapter “Linking of Spinlocks”. 
Updated HSI for S32K derivatives. 
Added chapter for exception context manipulation 
Fabian Wild 
Martin Schultheiß 
2017-06-19 2.5.0 Removed ORTI tracing from Os_Init and 
Os_InitMemory 
Support new Power PC Derivative: SPC574Sxx 
Torsten Schmidt 2017-06-06 2.6.0 Added descriptions for category 0 ISRs. 
Ivan Begert 
Senol Cendere 
2017-07-05 2.6.1 Chapter “ARM Special characteristic” extended. 
RH850 HSI extended. 
Updated Table 1-9 Supported RH850 Compilers. 
Updated Chapter 4.5.2 RH850 
Torsten Schmidt 2017-07-17 2.7.0 Chapter “Software Stack Check” extended. 
Chapter “VTT OS Specifics” extended. 
Chapter “Initialization of Interrupt Sources” 
extended. 
Chapter “Notes on Category 1 ISRs” extended. 
Chapter “Notes on Category 0 ISRs” extended. 
Chapter “Pre-Process Linker Command Files” 
added. 
API description of “Os_Init” extended. 
Senol Cendere 
Da He 
Andreas Jehl 
2017-08-15 2.8.0 Documented support for more RH850 derivatives 
and compiler versions. 
Updated documentations regarding location of OS 
identifiers. 
Support ARM CC (5.x) compiler for ARM Cortex-M 
Documented support of TC39x derivative with 
Tasking v6.0r1p2 compiler 
Martin Schultheiß 2017-08-17 2.9.0 Updated Derivative Support for PPC and RH850 
Senol Cendere 
Torsten Schmidt 
Rainer 
Künnemeyer 
2017-10-25 2.10.0 New vector timing hooks 
OS_VTHACTIVATION_LIMIT and 
OS_VTH_WAITEVENT_NOWAIT, usage of vector 
timing hooks now also in safety systems. Chapter 
“Task Stack Sharing” Extended 
Added comments on RTE interrupt API 
Da He 
Benjamin Seifert 
2017-11-13 2.11.0 Support GCC L

### Page 5

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 5 
based on template version 6.0.1 
objects"

### Page 6

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 6 
based on template version 6.0.1 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR Specification of Operating System 
Document ID 034: AUTOSAR_SWS_OS 
4.2.1 
[2] OSEK/VDX OSEK/VDX Operating System Specification 
This document is available in PDF-format on 
the Internet at the OSEK/VDX homepage 
(http://www.osek-vdx.org) 
2.2.3 
[3] OSEK/VDX OSEK RunTime Interface (ORTI) Part A: 
Language Specification. 
This document is available in PDF-format on 
the Internet at the OSEK/VDX homepage 
(http://www.osek-vdx.org) 
2.2 
[4] OSEK/VDX OSEK Run Time Interface (ORTI) Part B: OSEK 
Objects and Attributes 
This document is available in PDF-format on 
the Internet at the OSEK/VDX homepage 
(http://www.osek-vdx.org) 
2.2 
[5] Lauterbach ORTI Representation of SMP Systems (ORTI 
2.3) 
4 
[6] Vector vVIRTUALtarget Technical Reference See delivery 
information 
[7] Vector Startup with Vector and vVIRTUALtarget See delivery 
information 
[8] Vector MICROSAR VStdLib Technical Reference 
TechnicalReference_VStdLib_GenericAsr.pdf 
See delivery 
information 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 7

Technical Reference MICROSAR OS 
© 2017 Vector Informatik GmbH Version 2.12.0 7 
based on template version 6.0.1 
Contents 
1 Introduction................................ ................................ ................................ ................. 24 
1.1 Architecture Overview ................................ ................................ ...................... 24 
1.2 Abstract ................................ ................................ ................................ ........... 25 
1.3 Characteristics ................................ ................................ ...

*Excerpt: first 8 of 304 pages shown.*
