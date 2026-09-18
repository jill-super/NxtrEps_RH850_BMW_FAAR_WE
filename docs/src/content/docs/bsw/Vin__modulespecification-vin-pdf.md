---
title: 'Vin — ModuleSpecification_Vin'
description: 'Converted PDF document ModuleSpecification_Vin.pdf from module Vin.'
sidebar:
  hidden: true
---

> **Source:** `ModuleSpecification_Vin.pdf` (PDF, 638 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 38; title: -; author: -

## Converted content

### Page 1

Specification of Module Vin
Project BMW AUTOSAR Core 4 Rel. 2
Author BMW AG
Release Date 2017-02-23
Version 3.5.0
Status Released
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
Version Date Changed by Description
3.5.0 2017-02-23 Björn
Sachsenberg
No changes - only version update
3.4.2 2016-10-27 Björn
Sachsenberg
No changes - only version update
3.4.1 2016-08-25 Björn
Sachsenberg
No changes - only version update
3.4.0 2016-03-17 Björn
Sachsenberg
Added SWS IDs starting with SWS_Vin_0121,
changed SWS_Vin_0120
3.3.0 2015-12-11 Björn
Sachsenberg
No changes - only version update
3.2.0 2015-07-10 Björn
Sachsenberg
Added SI adapter, added SWS IDs from
SWS_Vin_0109 on
3.1.0 2015-03-13 Björn
Sachsenberg
Added SSV functionality from Fscsm, added SWS IDs
from SWS_Vin_0034 on
3.0.0 2014-10-29 Björn
Sachsenberg
Initial Release for SP2018.
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 1 of 38

### Page 2

Table of Contents
1 Introduction and functional overview 4
2 Acronyms and Abbreviations 4
3 Related documentation 5
3.1 BMW Specifications 5
3.2 AUTOSAR Specifications 5
4 Constraints and assumptions 6
5 Dependencies to other Modules 7
5.1 Dlog 7
5.2 Fscsm 7
5.3 RTE 7
6 Requirements traceability 8
7 Functional specification 9
7.1 Functional behavior 9
7.2 SSV 12
7.2.1 Secure environment 13
7.2.2 Challenge/response and CounterBase 13
7.2.3 Request/verify secure signal 14
7.2.4 SSV ports and interfaces 16
7.2.5 Message format 17
7.3 Error classification 18
7.4 Error detection 18
7.5 Error notification 18
8 API Specification 19
8.1 Imported types 19
8.2 Type definitions 19
8.3 Function definitions 19
8.3.1 Vin_Main 19
8.3.2 Vin_LifeCycleModeRequest 19
8.3.3 Vin_SsvOnVkEstablished 20
8.3.4 Vin_SsvReceiveResponseFromSss 20
8.3.5 Vin_SsvReceiveMac 20
8.3.6 Vin_SsvStateGet 21
8.3.7 Modes, Types and Mappings 21
8.3.8 Provided Interfaces 24
8.3.9 Expected Interfaces 26
8.3.10 Service Definition 28
8.3.11 Runnables and Entry Points 29
8.3.12 Runnables and Entry Points 30
9 Sequence Diagrams 31
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 2 of 38

### Page 3

10 Configuration 32
10.1 How to read this chapter 32
10.1.1 Configuration and configuration parameters 32
10.1.2 Variants 32
10.1.3 Containers 32
10.2 Containers and configuration parameters 33
10.2.1 CommonPublishedInformation 33
10.2.2 VinGeneral 34
10.2.3 SecureVin 36
10.2.4 MultiConfig 38
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 3 of 38

### Page 4

1 Introduction and functional overview
The Vin module is used to request the VIN over the bus, set the qualifier and hand it over to application
software components.
2 Acronyms and Abbreviations
API Application Programming Interface
AUTOSAR Automotive Open System Architecture
BNDB Bordnetzdatenbank BNE ist der aktuelle Begriff; BNDB ist veraltet, wird aber
gelegentlich noch gebraucht.
BNE Bord Netz Engineer
CAN Controller Area Network
DTC Diagnostic Trouble Code -> Fehlercode des Fehlerspeichereintrages
ECU Electronic Control Unit
EFS LH Eigenschafts- / Funktions- / Systemlastenheft
FAT Flash-Absicherungs-Tool
FZG Fahrzeug
GMT Greenwich Mean Time
HW Hardware
IEEE Institute of Electrical and Electronics Engineers Technisches Normungs-
gremium
IETF Internet Engineering Task Force Normungsgremium für Internet-Standards
IP Internet Protocol Netzwerkebene des TCP/IP Protokolls
ISO/OSI Schichtenmodell der Kommunikationsprotokolle
OS Operating System
PTP Precision Time Protocol
PWF Parken Wohnen Fahren Energie-Management Konzept bei BMW.
RTE Runtime Environment
SG Steuergerät
SGID Steuergeräte-ID, Diagnoseadresse, Steuergeräte-Adresse
SID Service Identifier
SW Software
SW-C Software Component
UDS Universal Diagnostic Services
VIN Vehicle Identification Number
All abbreviations used throughout this document -- except the ones listed here -- can be found in the
official AUTOSAR glossary [5].
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 4 of 38

### Page 5

3 Related documentation
3.1 BMW Specifications
[1] Specification of Module DataLogistic
ModuleSpecification_Dlog.pdf
[2] Specification of Module FSCSM
ModuleSpecification_Fscsm.pdf
[3] LH FP Teil 4 Codierung
SAP: 10001491-000-13
[4] Fahrzeug Security Client Security Module
SAP: 1000109600011
3.2 AUTOSAR Specifications
[5] Glossary
AUTOSAR_TR_Glossary
[6] Specification of RTE Software
AUTOSAR_SWS_RTE
[7] Layered Software Architecture
AUTOSAR_EXP_LayeredSoftwareArchitecture
[8] Specification of ECU Configuration
AUTOSAR_TPS_ECUConfiguration
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 5 of 38

### Page 6

4 Constraints and assumptions
[SWS_Vin_0001] ⌈There shall be only one Vin module available per ECU. ⌋()
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 6 of 38

### Page 7

5 Dependencies to other Modules
5.1 Dlog
The Dlog module [1] is used to get the internal VIN.
5.2 Fscsm
The Fscsm module [2] is needed for receiving the secure VIN.
5.3 RTE
The module Vin is realized as a software component and is using RTE services [6] for client/server as well
as sender/receiver communication to communicate with other SWCs.
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 7 of 38

### Page 8

6 Requirements traceability
The Requirements are taken from [3] and [4].
Requirement Description Satisfied by
[FP4_6292] No description [SWS_Vin_0002]
[FsCSM_1496] No description [SWS_Vin_0048]
[FsCSM_1497] No description [SWS_Vin_0048]
[FsCSM_1707] No description [SWS_Vin_0039]
[FsCSM_1708] No description [SWS_Vin_0039]
[FsCSM_1709] No description [SWS_Vin_0041]
[FsCSM_1710] No description [SWS_Vin_0039]
[FsCSM_391] No description [SWS_Vin_0078]
[FsCSM_4320] No description [SWS_Vin_0048]
[FsCSM_4336] No description [SWS_Vin_0049]
[FsCSM_4338] No description [SWS_Vin_0050]
[FsCSM_4418] No description [SWS_Vin_0056]
[FsCSM_4450] No description [SWS_Vin_0068]
[FsCSM_4451] No description [SWS_Vin_0069]
[FsCSM_4469] No description [SWS_Vin_0055]
[FsCSM_848] No description [SWS_Vin_0048]
[FsCSM_859] No description [SWS_Vin_0048]
[FsCSM_937] No description [SWS_Vin_0048]
[FsCSM_956] No description [SWS_Vin_0048]
ModuleSpecification_Vin, Version 3.5.0, Software Platforms Page 8 of 38

*Excerpt: first 8 of 38 pages shown.*
