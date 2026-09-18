---
title: 'Omc — OmcClassic_IntegrationManual'
description: 'Converted PDF document OmcClassic_IntegrationManual.pdf from module Omc.'
sidebar:
  hidden: true
---

> **Source:** `OmcClassic_IntegrationManual.pdf` (PDF, 232 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 12; title: -; author: -

## Converted content

### Page 1

Omc Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.2.0
Status Release
Hotline +49 89 382 - 32233
Contact bac@bmw.de
https://asc.bmw.com/jira/browse/BSUP (extern)
https://asc.bmwgroup.net/jira/browse/BSUP (intern)
Company
Bayerische
Motoren Werke
Aktiengesellschaft
Postal address
BMW AG
80788 München
Office address
Forschungs- und
Innovationszentrum
(FIZ)
Hufelandstr. 1
80937 München
Telephone
Switchboard
+49 89 382-0
Internet
www.bmwgroup.com
Revision History
Version Date Description
5.2.0 2017-12-14 BAC-6565: document callback mechanism to establish intrinsic safety
(AllowModeChange and OmcOperatingModeCallout)
5.1.1 2017-10-12 Version Update
5.1.0 2017-08-10 Version Update
5.0.0 2017-06-29 Initial version for SP2021
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 1 of 12

### Page 2

Table of Contents
1 Introduction 4
1.1 Functional overview 4
2 Related documentation 5
3 Limitations 6
4 Software Architecture 7
4.1 Dependencies on AUTOSAR modules 7
4.1.1 RTE 7
4.1.2 Det 7
4.1.3 Dcm 7
4.1.4 Dem 7
4.1.5 Nvm 7
4.2 Dependencies to other modules 7
5 Integration 8
5.1 Configuration of other Modules 8
5.1.1 Dcm 8
5.1.1.1 Read Data By Identifer 8
5.1.1.2 Routine Control 8
5.1.2 NvM 8
5.1.3 Dem 9
5.1.3.1 Enable Condition 9
5.1.3.2 Event 9
5.1.4 BswM 9
5.1.5 Det 9
5.2 Provided Interfaces 10
5.2.1 OmcOperatingMode and OmcExtendedOperatingMode 10
5.2.2 OmcModesCalloutsResult 10
5.3 Required Interfaces 10
5.3.1 OmcModesCallouts 10
5.4 Configuration 10
5.4.1 OmcGeneral 10
5.4.1.1 OmcDevErrorDetect 10
5.4.1.2 OmcOperatingModeCallout 11
5.5 Configuration of the RTE 11
5.5.1 Event Mapping 11
5.5.2 Data Mapping 11
5.5.2.1 Dcm 11
5.5.2.2 Det 11
5.5.3 Dem 11
5.5.4 NvM 11
5.5.5 BswM 11
5.5.6 Exclusive Areas 12
5.6 Software Integration 12
5.6.1 Startup/Initialization 12
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 2 of 12

### Page 3

5.6.2 Normal Operation 12
5.6.3 Shutdown/Deactivation 12
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 3 of 12

### Page 4

1 Introduction
This Integration Manual describes the basis functionality, API and the configuration and integration of the
BMW System Function Omc.
Functional overview
The main objective of the Omc functionality is to maintain the current Operating Mode of an ECU.
This means:
 Allowing the change of the current Operating Mode via diagnostic request
 Saving the current Operating Mode to Non Volatile RAM (NVRAM)
 Enabling/disabling Dem (more concrete: Setting/Unsetting a enable condition)
 Providing the current Operating Mode to other software components.
The Omc module distinguishes the following vehicle operating modes:
 NORMAL
 ASSEMBLY
 TRANSPORT
 FLASH
Note that in different documents these modes are sometimes called "energy modes" sometimes called
"operating modes". Although both terms are equivalent, we strictly use the term operating mode.
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 4 of 12

### Page 5

2 Related documentation
References
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 5 of 12

### Page 6

3 Limitations
No limitations are known.
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 6 of 12

### Page 7

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module Omc depends on the following BSW modules:
RTE
As a software component, the Omc module uses Rte client/server communication to communicate with
other SWCs and BSW. Additionally the scheduling is done by the Rte.
Det
In case Det usage is enabled in the Omc configuration, Omc will report development errors by using the
Det functionality.
Dcm
The Dcm will call functionality of the Omc module when a RDBI for the operating mode or the extended
operating mode has been received. The corresponding R-ports of the Dcm for these two identifiers must
be connected with the corresponding P-ports of the Omc.
Dem
The Omc use the operation SetEventStatus of the CSI DiagnosticMonitor to set an Event via Rte. It also
uses the ClientServer Interface of service EnableCondition.
Nvm
The Omc relies on services provided by the Nvm to store its persistent data regarding the current
operating mode and current extended operating mode.
Dependencies to other modules
Omc does not have dependencies to other modules.
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 7 of 12

### Page 8

5 Integration
Configuration of other Modules
The following modules shall be configured, before this module can be generated, compiled and linked.
Dcm
Read Data By Identifer
[] ⌈Two Read Data By Identifier commands shall be configured within Dcm (22 10 0A and 22 10 0E).
⌋(DK_T3_736, DK_T3_762, FZM_SC_SYS_PA_335, DK_T3_1255)
 DcmDspDataSize shall be set to 8
 DcmDspDataUsePort shall be set to USE_DATA_SYNCH_CLIENT_SERVER
 DID shall be configured to be read in all sessions and security levels
Routine Control
[] ⌈Two Routine Control commands shall be configured within Dcm (31 01 0F 0C and 31 01 10 03).
⌋(DK_T3_720, DK_T3_725, DK_T3_727, DK_T3_729, DK_T3_751, FZM_SC_SYS_PA_334,
FZM_SC_SYS_PA_334)
 DcmDspRoutineFixedLength shall be true
 DcmDspRoutineUsePort shall be true
 Only DcmDspStartRoutineIn shall be configured
 DcmDspRoutineSignalLength shall be set to 8
 DcmDspRoutineSignalPos shall be set to 0
NvM
The Omc needs a Nvm block to store the operating mode:
[] ⌈
 block size shall be set to 2 bytes
 Ram block address shall be set to Omc_NvData
 Rom block address shall be set to Omc_DefaultNvData
 NvmBlockManagementType shall be set to NVM_BLOCK_NATIVE
 NvmBlockUseCrc shall be disabled
 NvmSelectBlockForReadall shall be set to true
⌋(DK_T3_743, FZM_SC_SYS_PA_169, FZM_SC_SYS_PA_329, FZM_SC_SYS_PA_171,
FZM_SC_SYS_PA_331)
OmcClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 8 of 12

*Excerpt: first 8 of 12 pages shown.*
