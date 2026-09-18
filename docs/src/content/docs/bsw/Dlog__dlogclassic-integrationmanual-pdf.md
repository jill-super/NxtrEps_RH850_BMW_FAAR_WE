---
title: 'Dlog — DlogClassic_IntegrationManual'
description: 'Converted PDF document DlogClassic_IntegrationManual.pdf from module Dlog.'
sidebar:
  hidden: true
---

> **Source:** `DlogClassic_IntegrationManual.pdf` (PDF, 249 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 17; title: -; author: -

## Converted content

### Page 1

Dlog Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.3.1
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
5.3.1 2017-12-14 Update NvM configuration
5.3.0 2017-11-09 Version Update
5.2.1 2017-10-12 Fix RDBI commands
5.2.0 2017-09-14 Fix RDBI commands
5.1.0 2017-08-10 Remove deprecated stuff, change FirstStartFlag to ProgId
5.0.0 2017-06-29 Initial version for SP2021
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 1 of 17

### Page 2

Table of Contents
1 Introduction 4
1.1 General 4
1.2 Functional overview 4
2 Acronyms and Abbreviations 5
3 Related documentation 6
4 Limitations 7
5 Software Architecture 8
5.1 Dependencies on AUTOSAR modules 8
5.1.1 CRC Library 8
5.1.2 DCM 8
5.1.3 MemIf 8
5.1.4 NvM 8
5.1.5 RTE 8
5.2 Dependencies on BMW modules 8
5.2.1 Bootmanager 8
5.2.2 BUtil 8
5.2.3 Coding 9
5.2.4 DlogUser 9
6 Integration 10
6.1 Configuration of other Modules 10
6.1.1 Dcm 10
6.1.1.1 Read Data By Identifier 10
6.1.1.2 Routine Control 10
6.1.2 Nvm 11
6.1.3 MemIf 12
6.2 Configuration 12
6.2.1 DlogGeneral 12
6.2.2 DlogFeatures 13
6.2.3 DlogUser 13
6.2.4 DlogSharedGeneral 13
6.2.4.1 Logistic 13
6.2.5 DlogSharedInterface 13
6.2.6 DlogSharedPlatform 13
6.3 ECC error handling 14
6.4 Configuration of the RTE 14
6.5 Software Integration 15
6.5.1 Startup/Initialisation 15
6.5.1.1 Preconditions 15
6.5.1.2 Postconditions 15
6.5.2 Normal Operation 15
6.5.3 Shutdown/Deactivation 15
6.5.3.1 Preconditions 15
6.5.3.2 Postconditions 15
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 2 of 17

### Page 3

6.5.4 Memory Mapping 16
7 Post Integration 17
7.1 SWE Generator Config File 17
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 3 of 17

### Page 4

1 Introduction
General
For a general introduction to the BAC4/aBAC Modules please refer to [1].
This document only describes topics related to the Dlog BAC4/aBAC Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW system
function Dlog.
Functional overview
The Data Logistic is part of the BootManager, Bootloader and Application. It is needed for every ECU to
 get production information
 identify software and hardware
 check compatibility of hardware and software
 check compatibility of all software units (SWEs)
 check at startup if the software is valid and may be started.
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 4 of 17

### Page 5

2 Acronyms and Abbreviations
API Application Programming Interface
Application Application stands for the high-level part of software that uses the APIs
provided by the modules. It can also mean the driving application that does
not belong to the Bootloader.
AUTOSAR Automotive Open System Architecture
CCC Car Communication Computer
Central Pia Master Central instance controlling and managing Pia functionality (PIA-
Zentralinstanz).
Coding Coding Client
DTC Diagnostic Trouble Code -> Fehlercode des Fehlerspeichereintrages
ECU Electronic Control Unit
FAT Flash-Absicherungs-Tool
FZG Fahrzeug
HO Handelsorganisation (BMW)
HW Hardware
IDRL Individual Data Recovery - light
OS Operating System
Pia Personalisierung, Individualisierung, Adaption (Personalization, Individualiza-
tion, Adaptation)
Pia value Scalar setting used by a Pia function.
PiaClient Basic software module providing services for Pia functions.
Profile Union of all personal Pia values.
RAM Block The part of an NVRAM Block that resides in the RAM. A RAM block is
used as shared memory interface between the NVRAM manager and the
PiaClient.
RTE Runtime Environment
SG Steuergerät
SGID Steuergeräte-ID, Diagnoseadresse, Steuergeräte-Adresse
SID Service Identifier
SW Software
SW-C Software Component
UDS Universal Diagnostic Services
VIN Vehicle Identification Number
VIN7 The last 7 digits of the 17-digit VIN
All abbreviations used throughout this document -- except the ones listed here -- can be found in the
official AUTOSAR glossary [2].
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 5 of 17

### Page 6

3 Related documentation
References
[1] BAC4 General Concept for the Module Integration
BAC4_General_Concepts_for_the_Module_Integration.pdf
[2] Glossary
AUTOSAR_TR_Glossary
[3] Specification of CRC Routines
AUTOSAR_SWS_CRCLibrary
[4] Specification of Diagnostic Communication Manager
AUTOSAR_SWS_DiagnosticCommunicationManager
[5] Specification of Memory Abstraction Interface
AUTOSAR_SWS_MemoryAbstractionInterface
[6] Specification of NVRAM Manager
AUTOSAR_SWS_NVRAMManager
[7] Specification of RTE Software
AUTOSAR_SWS_RTE
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 6 of 17

### Page 7

4 Limitations
Dlog has been validated on HWs where erased flash cells can be read without triggering a ECC exception.
Nevertheless it should also run on other types of HWs, see section 6.3, ‘‘ECC error handling’’ for details.
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 7 of 17

### Page 8

5 Software Architecture
Dependencies on AUTOSAR modules
CRC Library
In the Bootmanager, the CRC Library [3] is used for checking the SWEs against data corruption.
DCM
The module Dcm [4] will call functionality of the module DataLogistic when a ReadDataByIdentifier,
WriteDataByIdentifier or RoutineControl has been received for an logistic operation. In Application the
corresponding R-ports of the Dcm for these operations shall be connected with the corresponding
P-ports of the module DataLogistic. In Bootloader the Dcm calls the C-Api of DataLogistic.
MemIf
In Bootloader, the NV-RAM blocks are initialized via MemIf [5].
NvM
In Application, the NV-RAM blocks are initialized through the NvM [6].
RTE
Only in Application the module DataLogistic is realized as a software component and is using RTE
services [7] for client/server as well as sender/receiver communication to communicate with other SWCs.
Dependencies on BMW modules
Bootmanager
In Bootmanager, the file Bmhw_Platform_Cfg.h is #included. It must define the function
BM_CLEAR_HARDWARE_ECC_ERROR_FLAG().
BUtil
The BUtil library provides utility functions used by Dlog.
DlogClassic_IntegrationManual.pdf, Version 5.3.1, Software Platforms Page 8 of 17

*Excerpt: first 8 of 17 pages shown.*
