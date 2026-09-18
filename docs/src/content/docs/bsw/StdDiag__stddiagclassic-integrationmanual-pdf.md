---
title: 'StdDiag — StdDiagClassic_IntegrationManual'
description: 'Converted PDF document StdDiagClassic_IntegrationManual.pdf from module StdDiag.'
sidebar:
  hidden: true
---

> **Source:** `StdDiagClassic_IntegrationManual.pdf` (PDF, 283 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 30; title: -; author: -

## Converted content

### Page 1

StdDiag Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.4.0
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
5.4.0 2017-12-14 BAC-6257: Add integration of functionality "Application Data
Transfer" (ADT)
5.3.0 2017-11-09 BAC-6249: Move SgbdIndex to adapter part and add post build
support
5.2.0 2017-10-12 Version Update
5.1.0 2017-08-10 Version Update
5.0.0 2017-06-08 Initial version for SP2021
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 1 of 30

### Page 2

Table of Contents
1 Introduction 4
1.1 Functional overview 4
2 Related documentation 5
3 Limitations 6
3.1 Unreleased Dlt specification in AUTOSAR 6
4 Software Architecture 7
4.1 Dependencies on AUTOSAR modules 7
4.1.1 RTE 7
4.1.2 Det 7
4.1.3 Dcm 7
4.1.4 Dem 7
4.1.5 BswM 7
4.1.6 Dlt 7
4.1.7 EcuC 8
4.2 Dependencies to other modules 8
4.2.1 Darh 8
4.2.2 Omc 8
4.2.3 Stm 8
4.2.4 Other SWC 8
5 Integration 9
5.1 Configuration of other Modules 9
5.1.1 Dcm 9
5.1.1.1 Read Data By Identifier 9
5.1.1.2 RoutineControl 11
5.1.1.3 Service Request Manufacturer Notification 16
5.1.1.4 Service Handler for Upload Download Services 16
5.1.2 Det 17
5.1.3 Dem 17
5.1.4 BswM 17
5.1.5 EcuC 20
5.2 Configuration of generic part 20
5.2.1 StdDiagGeneral 20
5.2.1.1 StdDiagDevErrorDetect 20
5.2.1.2 StdDiagUserEstablishIntrinsicSafety 20
5.2.1.3 StdDiagUserActiveSessionState 21
5.2.2 StdDiagUserProgrammingPreconditionsCheck 21
5.2.2.1 MaxNumberUserProgrammingPrecondition 21
5.2.3 StdDiagProvideIDRL 21
5.2.3.1 DIDTableFormatIdentifier 22
5.2.3.2 IDRLClient 22
5.3 Configuration of adapter part 22
5.3.1 StdDiagGeneral 22
5.3.1.1 StdDiagClearSecondaryErrorMemory 22
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 2 of 30

### Page 3

5.3.2 StdDiagUserDefinedMemory 23
5.3.2.1 StdDiagUserDefinedMemoryName 23
5.3.2.2 StdDiagUserDefinedMemoryId 23
5.3.3 StdDiagSgbdIndex 23
5.3.3.1 SgbdIndex 23
5.3.4 StdDiagApplicationDataTransfer 24
5.3.4.1 ApplicationRoutineControlIdentifier 24
5.3.4.2 RoutineIdentifierValue 24
5.3.4.3 ApplicationSubRoutineControlIdentifier 24
5.3.4.4 SubRoutineIdentifierValue 24
5.3.4.5 controlIDs 24
5.3.5 StdDiagProvideDLTSupport 24
5.3.5.1 StdDiagNumberSupportedDLTLogChannels 25
5.4 Configuration of the RTE 25
5.4.1 Assembly Software Connectors 25
5.4.1.1 Dcm 25
5.4.1.2 Dem 26
5.4.1.3 Det 27
5.4.1.4 Darh 27
5.4.1.5 Omc 27
5.4.1.6 Stm 27
5.4.1.7 BswM 27
5.4.1.8 Other Application SWC 28
5.4.2 Event Mapping 29
5.4.3 Data Mapping 29
5.4.4 Exclusive Areas 29
5.5 Software Integration 29
5.5.1 Startup/Initialization 29
5.5.2 Normal Operation 29
5.5.3 Shutdown/Deactivation 29
5.5.4 Select Post Build Configuration 29
5.5.5 SWCD 30
5.5.6 Prevent sleep mode 30
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 3 of 30

### Page 4

1 Introduction
This Integration Manual describes the basic functionality of the BMW system function "Standard
Diagnostics" (StdDiag), the configuration of the StdDiag module and of dependant modules, and the
integration of the StdDiag module into BAC4 or aBAC.
Functional overview
The main functionality of the StdDiag module is to handling the active session states ("subsessions") of
the default diagnostic session and the extended diagnostic session. It ensures that the programming
preparation process (i.e. the transition from the diagnostic default session via the extended diagnostic
session to the programming session) is only successful, if the diagnostic requests are received in the
correct sequence and all necessary preconditions are fulfilled. It also checks whether diagnostic requests
shall be rejected or allowed in the different session states.
The StdDiag module also provides diagnostic service handlers for
 clearing the secondary error memory
 reading the active session state
 reading the programming preconditions
 reading the SGBD-Index
 diagnostic communication loopback functionality
 handling Diagnostic Log and Trace settings
 handling IDRL basic functionality
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 4 of 30

### Page 5

2 Related documentation
References
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 5 of 30

### Page 6

3 Limitations
Unreleased Dlt specification in AUTOSAR
StdDiag optionally uses services of the AUTOSAR BSW module Dlt (Diagnostic Log and Trace). The
specification of the ClientServer-Interface "DLTService", which provides the services used by StdDiag, is
released with AUTOSAR 4.3.0. As required in the document "AUTOSAR features for SP2021", projects
using Dlt shall support Dlt based on AUTOSAR 4.3.
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 6 of 30

### Page 7

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module StdDiag depends on the following BSW modules:
RTE
As a software component, the StdDiag module uses Rte client/server and sender/receiver communication
to communicate with other SWCs and BSW modules.
Det
StdDiag optionally reports development errors to the Det.
Dcm
StdDiag is tightly coupled with the Dcm. The StdDiag implements several RDBI/WDBI and RC services,
as well as services for upload download functionality. Dcm shall be configured in a way, that it dispatches
theses jobs to the StdDiag SWC. In addition, the StdDiag requests information about the current
diagnostic session.
Moreover the StdDiag receives information about incoming requests and the corresponding result of the
request via a Manufacturer Notification. The StdDiag uses this feature to accept / deny a number of
requests, and to handle the active session state.
Dem
StdDiag sets an EnableCondition to allow / deny writing of error entries and clears DTCs in the secondary
error memory.
BswM
StdDiag receives and requests mode switches from the BswM to switch the current StdDiag operational
mode. It further requests Communication Control mode switches, and receives a mode switch from the
BswM when the active diagnostic session has changed.
Dlt
StdDiag optionally receives diagnostic requests for Diagnostic Log and Trace control and forwards them
to the Dlt service interface.
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 7 of 30

### Page 8

EcuC
StdDiag provides post build configurable parameters. If post build support is used, an EcuC configuration
is needed to evaluate available variants.
Dependencies to other modules
Darh
The StdDiag suspends / resumes sending Response on Events.
Omc
The StdDiag needs the current operating mode and extended operating mode from the Omc module. In
addition, StdDiag provides a handler to allow / deny changing the operating mode.
Stm
The StdDiag reads the current PWF state from the Stm.
Other SWC
The StdDiag optionally calls another Application Software Component to establish intrinsic safety and to
check the users programming preconditions.
The StdDiag optionally calls another Application Software Component to get the active session state in
Sessions that have their own active session handling.
The StdDiag calls another Application Software Component (e.g. PiaClient) to read, write or reset the
individual data, if the feature "Individual Data Recovery Light" (IDRL) is activated.
The StdDiag calls another Application Software Component (e.g. Bs) to upload or download application
data, if the feature "Application Data Transfer" (ADT) is activated.
StdDiagClassic_IntegrationManual.pdf, Version 5.4.0, Software Platforms Page 8 of 30

*Excerpt: first 8 of 30 pages shown.*
