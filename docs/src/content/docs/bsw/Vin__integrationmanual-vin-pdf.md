---
title: 'Vin — IntegrationManual_Vin'
description: 'Converted PDF document IntegrationManual_Vin.pdf from module Vin.'
sidebar:
  hidden: true
---

> **Source:** `IntegrationManual_Vin.pdf` (PDF, 236 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 11; title: -; author: -

## Converted content

### Page 1

Integration Manual Vin
Project BMW AUTOSAR Core 4 Rel. 2
Author BMW AG
Release Date 2017-02-23
Version 3.5.0
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
Version Date Changed by Description
3.5.0 2017-02-23 Björn
Sachsenberg
No changes - only version update
3.4.2 2016-10-27 Björn
Sachsenberg
Add a note on NVM block length
3.4.1 2016-08-25 Björn
Sachsenberg
Fix NVM configuration
3.4.0 2016-03-17 Björn
Sachsenberg
Specify write frequency of NVM blocks, updated
section Data Mapping
3.3.0 2015-12-11 Björn
Sachsenberg
Clarified data mapping
3.2.0 2015-07-10 Björn
Sachsenberg
Added SI adapter
3.1.0 2015-03-13 Björn
Sachsenberg
Added SSV functionality
3.0.0 2014-10-29 Björn
Sachsenberg
Initial version
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 1 of 11

### Page 2

Table of Contents
1 Introduction 3
1.1 General 3
1.2 Functional overview 3
2 Acronyms and Abbreviations 3
3 Related documentation 5
3.1 BMW Specifications 5
3.2 AUTOSAR Specifications 5
4 Limitations 6
5 Software Architecture 7
5.1 Dependencies on AUTOSAR modules 7
5.1.1 RTE 7
5.1.2 NvM 7
5.2 Dependencies on BMW modules 7
5.2.1 Dlog 7
5.2.2 Fscsm 7
6 Integration 8
6.1 Configuration of other Modules 8
6.1.1 Communication Stack 8
6.1.2 Nvm 8
6.1.3 Fscsm 9
6.2 Configuration 9
6.3 Configuration of the RTE 9
6.3.1 Assembly connectors 9
6.3.1.1 Always 9
6.3.1.2 If SecureVin is configured 9
6.3.2 Event Mapping 9
6.3.3 Data Mapping 10
6.3.3.1 If EnableSIAdapter=false 10
6.3.3.2 If SecureVin is configured with EnableSIAdapter=false 10
6.3.3.3 If EnableSIAdapter=true 10
6.3.3.4 If SecureVin is configured with EnableSIAdapter=true 10
6.3.4 Exclusive Areas 11
6.4 Software Integration 11
6.4.1 Startup/Initialisation 11
6.4.2 Normal Operation 11
6.4.3 Shutdown/Deactivation 11
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 2 of 11

### Page 3

1 Introduction
1.1 General
For a general introduction to the BAC4 Platform Modules please refer to [1].
This document only describes topics related to the SWT BAC4 Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW system
function VIN.
1.2 Functional overview
The Vin module is used to request the VIN over the bus, set the qualifier and hand it over to application
software components.
2 Acronyms and Abbreviations
A&S Authentication and Signature (Grundschutzmechanismen)
AllgGB Allgemeine Gültigkeitsbedingung
AN Applikationsnummer
API Application Programming Interface
AppGB Applikationsspezifische Gültigkeitsbedingung
AUTOSAR Automotive Open System Architecture
CA Certification Authority
CAL Cryptographic Abstraction Layer
CAS Car Access System (Steuergerät)
CCC Car Communication Computer
CKD Completely Knocked Down. A BMW plant that is not connected to the
central BMW IT.
CSM Client Security Module
CRL Certificate Revocation List
DEK Data Encryption Key
DER Distinguished Encoding Rules (As described by ASN.1)
DES Data Encryption Standard
DN Distinguished Name
DTC Diagnostic Trouble Code -> Fehlercode des Fehlerspeichereintrages
ECU Electronic Control Unit
FAT Flash-Absicherungs-Tool
FSC Freischaltcode
FSCS Freischaltcode-Stelle
FZG Fahrzeug
FZG-R BMW Fahrzeug-Root-CA
GB Gültigkeitsbedingung
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 3 of 11

### Page 4

GG Gültigkeitsgruppe
GMT Greenwich Mean Time
HO Handelsorganisation (BMW)
HW Hardware
M-FSCS Master-Freischaltcodestelle
OS Operating System
PKI Public Key Infrastrucutre
RCn Routine Control Option n / Exit Result n
RI Routine Identifier
RSA Asymmetric Cryptoalgorithm by Rivest, Shamir und Adleman
RTE Runtime Environment
SG Steuergerät
SGID Steuergeräte-ID, Diagnoseadresse, Steuergeräte-Adresse
SID Service Identifier
SigS SW-Signatur-Stelle
SW Software
SW-C Software Component
SWID Software-ID consisting of application number and upgrade index
SWT SWEEPING Technologies (SoftWare Enabled Electronic Platform for Inno-
vative Next Generation Technologies)
UDS Universal Diagnostic Services
UI Upgrade Index
UTC Coordinated Universal Time
VCM Vehicle Configuration Management
VIN Vehicle Identification Number
VIN7 The last 7 digits of the 17-digit VIN
All abbreviations used throughout this document -- except the ones listed here -- can be found in the
official AUTOSAR glossary [6].
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 4 of 11

### Page 5

3 Related documentation
3.1 BMW Specifications
[1] BAC4 General Concept for the Module Integration
BAC4_General_Concepts_for_the_Module_Integration.pdf
[2] Specification of Module DataLogistic
ModuleSpecification_Dlog.pdf
[3] Specification of Module FSCSM
ModuleSpecification_Fscsm.pdf
[4] Integration Manual FSCSM
IntegrationManual_Fscsm.pdf
[5] Specification of Module Vin
ModuleSpecification_Vin.pdf
3.2 AUTOSAR Specifications
[6] Glossary
AUTOSAR_TR_Glossary
[7] Specification of RTE Software
AUTOSAR_SWS_RTE
[8] Specification of NVRAM Manager
AUTOSAR_SWS_NVRAMManager
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 5 of 11

### Page 6

4 Limitations
Autosar 4.2.1 or later is required.
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 6 of 11

### Page 7

5 Software Architecture
5.1 Dependencies on AUTOSAR modules
5.1.1 RTE
The module Vin is realized as a software component and is using RTE services [7] for client/server as well
as sender/receiver communication to communicate with other SWCs.
5.1.2 NvM
The NVRAM Manager [8] is used to store the last VIN and the SSV state.
5.2 Dependencies on BMW modules
5.2.1 Dlog
The Dlog module [2] is used to get the internal VIN.
5.2.2 Fscsm
The Fscsm module [3] is needed for receiving the secure VIN.
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 7 of 11

### Page 8

6 Integration
6.1 Configuration of other Modules
The following modules shall be configured, before the module Vin is compiled and linked.
6.1.1 Communication Stack
The communication stack shall be configured to provide the Vehicle Identification Number (VIN) message
from the corresponding bus.
For i∈{ 1, . . . ,7} configure the signals
Shortname (according to BMW BNE): NO_VECH_< i>
ComBitPosition: 8(i− 1)
ComBitSize: 8
ComSignalEndianness: OPAQUE
ComSignalLength: 1
ComSignalType: UINT8_N
ComTransferProperty: TRIGGERED
Note: The Signals NO_VECH_< i> (1≤ i≤ 7) have to be configured as a Signalgroup!
Note: In Ethernet, these signals are modeled as structure in the field ChassisNumber of the Service
Interface VehicleInformation.
6.1.2 Nvm
Following NvM blocks shall be configured:
NVM_BLOCK_Vin
NvMBlockCrcType NVM_CRC16
NvMBlockHeaderInclude Vin_NvM.h
NvMBlockManagementType NVM_BLOCK_NATIVE
NvMBlockUseCrc true
NvMBlockWriteProt false
NvMExtraBlockChecks true
NvMNvBlockLength 81
NvMNvBlockNum 1
NvMProvideRteServicePort true
NvMRamBlockDataAddress -
NvMResistantToChangedSw true, if NvMDynamicConfiguration = true
NvMRomBlockDataAddress &Vin_NVStateDefault
NvMRomBlockNum 0
1block length might differ depending on the used compiler and compiler settings
IntegrationManual_Vin, Version 3.5.0, Software Platforms Page 8 of 11

*Excerpt: first 8 of 11 pages shown.*
