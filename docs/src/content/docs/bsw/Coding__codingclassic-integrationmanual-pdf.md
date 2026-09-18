---
title: 'Coding — CodingClassic_IntegrationManual'
description: 'Converted PDF document CodingClassic_IntegrationManual.pdf from module Coding.'
sidebar:
  hidden: true
---

> **Source:** `CodingClassic_IntegrationManual.pdf` (PDF, 237 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 23; title: -; author: -

## Converted content

### Page 1

Coding Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.2.1
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
5.2.1 2017-12-14 Version Update
5.2.0 2017-11-09 Version Update
5.1.0 2017-10-12 Version Update
5.0.1 2017-09-14 Version Update
5.0.0 2017-06-08 Initial version for SP2021
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 1 of 23

### Page 2

Table of Contents
1 Introduction 4
1.1 General 4
1.2 Functional overview 4
2 Related documentation 5
3 Limitations 6
4 Software Architecture 7
4.1 Dependencies on AUTOSAR modules 7
4.1.1 NvM 7
4.1.2 Dem 7
4.1.3 Dcm 7
4.1.4 Com 7
4.1.5 Det 7
4.1.6 RTE 7
4.1.7 BswM 7
4.2 Dependencies to other modules 8
4.2.1 Dlog 8
4.2.2 Vin 8
4.2.3 Other SWC 8
5 Integration 9
5.1 Configuration of other Modules 9
5.1.1 NvM 9
5.1.2 Dem 9
5.1.3 Dcm 10
5.1.3.1 DiagnosticSession 10
5.1.3.2 DiagnosticSessionControl 10
5.1.3.3 RoutineControl 11
5.1.3.4 ReadDataByIdentifier 12
5.1.3.5 DiagnosticSessionControl 14
5.1.3.6 Service Request Manufacturer Notification 15
5.1.4 Com 15
5.1.5 Det 15
5.1.6 BswM 15
5.2 Configuration of generic part 16
5.2.1 CodingCrypto 16
5.2.1.1 CryptoLib 16
5.2.1.2 Csm 16
5.2.2 CodingGeneral 16
5.2.2.1 CodingDevErrorDetect 16
5.2.2.2 CodingSignatureSize 17
5.2.2.3 CodingCryptoEnable 17
5.2.2.4 CodingProdErrorCEUDDetection 17
5.2.2.5 CodingConditionCheck 17
5.2.2.6 CodingReceiveBufferSize 17
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 2 of 23

### Page 3

5.2.2.7 CodingSendBufferSize 18
5.2.3 CodingArea 18
5.2.3.1 CodingAreaDefVal 18
5.3 Configuration of adapter part 20
5.3.1 CodingClassicGeneral 20
5.3.1.1 CodingCycleTime 20
5.3.1.2 Other Application SWC 20
5.3.2 Event Mapping 21
5.3.3 Data Mapping 21
5.3.4 Exclusive Areas 21
5.4 Software Integration 22
5.4.1 Startup/Initialization 22
5.4.2 Normal Operation 22
5.4.3 Shutdown/Deactivation 22
5.4.4 SWCD 22
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 3 of 23

### Page 4

1 Introduction
The Coding system consists of a Coding module that is part of the ECU application and the Coder.
Almost in the same manner as the Bootloader programs the ROM of an ECU, the Coding module codes
the NV memory of an ECU with vehicle specific data derived from the vehicle description document e.g.
type key, extra equipment, country specifics, year of model/construction stage, additional comments or
service upgrade options.
General
For a general introduction to the BAC4/aBAC Modules please refer to [1].
This document only describes topics related to the Coding BAC4/aBAC Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW system
function Coding.
Functional overview
The Coding module implements the coding process that is part of the vehicle programming process. It
provides functions to the application to read coded data stored in the NV memory. If the NV memory
contains no valid data default values are provided. The coded data in NV memory can only be changed via
a diagnostic coding session.
The Coding module provides the following functionalities:
 Manages coding data stored in NV memory
 Provides read/write access via a special UDS diagnostics Session to the Coder
 Provides read only access via API to the ECU application
 Informs the ECU application about its current status
 Performs signature checks over the Coding data
 Restores safe default values in case of errors
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 4 of 23

### Page 5

2 Related documentation
References
[1] BAC4 General Concept for the Module Integration
BAC4_General_Concepts_for_the_Module_Integration.pdf
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 5 of 23

### Page 6

3 Limitations
 The Coding module supports only one asymmetric key to calculate the signature for all Coding areas.
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 6 of 23

### Page 7

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module Coding depends on the following BSW modules:
NvM
The Coding module uses the NVM to read Coding data from NV memory and to write it back.
Dem
The Coding module uses the DEM API to report critical events and write error memory entries.
Dcm
The Coding module uses the DCM to communicate with the Coder by sending and receiving diagnostic
UDS messages via CAN, FlexRay, etc.
Com
The Coding module use signals from COM to get the Vehicle Speed.
Det
The Coding module optionally reports development errors to the Det.
RTE
As a software component, the Coding module uses Rte client/server and sender/receiver communication
to communicate with other SWCs and BSW modules.
BswM
The Coding receives and requests mode switches from the BswM to switch the current Coding
operational mode. It further receives a mode switch from the BswM when the active diagnostic session
has changed and when the bus communication status has changed.
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 7 of 23

### Page 8

Dependencies to other modules
Dlog
The Dlog module is used to obtain the information during startup if the control unit has been coded after
flash programming.
Vin
The Vin module is used to obtain the current bus VIN.
Other SWC
The Coding optionally calls another Application Software Component to perform a plausibility check of
the net coding data received during the coding data transaction if implausible net coding data can lead to
safety-critical states of the control unit.
CodingClassic_IntegrationManual, Version 5.2.1, Software Platforms Page 8 of 23

*Excerpt: first 8 of 23 pages shown.*
