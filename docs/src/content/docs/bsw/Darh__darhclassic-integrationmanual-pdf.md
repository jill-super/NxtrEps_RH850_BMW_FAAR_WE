---
title: 'Darh — DarhClassic_IntegrationManual'
description: 'Converted PDF document DarhClassic_IntegrationManual.pdf from module Darh.'
sidebar:
  hidden: true
---

> **Source:** `DarhClassic_IntegrationManual.pdf` (PDF, 237 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 13; title: -; author: -

## Converted content

### Page 1

Darh Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.1.0
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
5.1.0 2017-12-14 JC-42 Document use of the Com port
5.0.2 2017-11-09 JC-42 Version Update
5.0.1 2017-10-12 JC-42 Version Update
5.0.0 2017-04-13 Mariano
Cerdeiro
Initial version for SP2021
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 1 of 13

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
5.1.3.1 Event 9
5.1.4 Det 9
5.1.5 BswM 9
5.1.6 Com 10
5.2 Configuration 10
5.2.1 DarhGeneral 10
5.2.1.1 DarhDevErrorDetect 10
5.2.1.2 DarhQueueHandlerCycleTime 10
5.2.2 DarhQueueSize 10
5.2.3 DarhActiveReportListType 10
5.2.4 DarhActiveReportedEvent 11
5.3 Configuration of the RTE 11
5.3.1 Event Mapping 11
5.3.2 Data Mapping 11
5.3.2.1 Dcm 11
5.3.2.2 Det 11
5.3.3 Dem 11
5.3.4 NvM 12
5.3.5 BswM 12
5.3.6 NvM 12
5.3.7 User SWC 12
5.3.8 Exclusive Areas 12
5.4 Software Integration 12
5.4.1 Startup/Initialization 13
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 2 of 13

### Page 3

5.4.2 Normal Operation 13
5.4.3 Shutdown/Deactivation 13
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 3 of 13

### Page 4

1 Introduction
This Integration Manual describes the basis functionality, API and the configuration and integration of the
BMW System Function Darh.
Functional overview
The main objective of the Darh functionality is to send errors that occurred locally in the ECU and are
reported to the Dem to a central master over the system bus. The idea is to collect errors of the individual
ECUs in the vehicle in one central place to allow later analysis of error correlations between the different
ECUs.
For this purpose, errors are sent to the master containing timestamp information. This allows deducing
the order in which errors occurred in the complete system and helps to find out the original reason of a
complex causal loop.
The Darh module itself is modeled as an AUTOSAR software component (SWC).
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 4 of 13

### Page 5

2 Related documentation
References
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 5 of 13

### Page 6

3 Limitations
No limitations are known.
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 6 of 13

### Page 7

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module Darh depends on the following BSW modules:
RTE
As a software component, the Darh module uses RTE client/server communication to communicate with
other SWCs and BSW. Additionally the scheduling is done by the RTE.
Det
In case Det usage is enabled in the Darh configuration, Darh will report development errors by using the
Det functionality.
Dcm
The Darh is tightly coupled with the Dcm. The Darh implements certain RDBI and RC services. Dcm shall
be configured in a way, that it dispatches theses jobs to the Darh SWC.
Dem
The Darh receives general callbacks of the Dem in case event related data changed. Additionally the Darh
controls specific events via ClientServerInterface DiagnosticMonitor of the Dem.
Nvm
The Darh uses the NvM to store and read the content of the error queue which shall be stored on non
volatile memory at shutdown and restored at startup. Darh also stores if the tranmission is enabled or not.
Dependencies to other modules
Darh does not have dependencies to other modules.
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 7 of 13

### Page 8

5 Integration
Configuration of other Modules
The following modules shall be configured, before this module can be generated, compiled and linked.
Dcm
Read Data By Identifer
The RDBI command 22 17 23 shall be configured within Dcm:
 DcmDspDataSize shall be long enough to store the complete list of DTC configured within Darh
(DarhActiveReportedEvent). Greater than count of DarhActiveReportedEvent * 3.
 DcmDspDataInfoRef shall reference to DcmDspDataInfo with DcmDspDataFixedLength set to false
 DcmDspDataUsePort shall be set to USE_DATA_SYNCH_CLIENT_SERVER
 DID shall be configured to be read in all sessions and security levels
Routine Control
Two Routine Control command shall be configured within Dcm.
One used to trigger two Dummy DTCs (31 01 03 04):
 DcmDspRoutineFixedLength shall be true
 DcmDspRoutineUsePort shall be true
 Only DcmDspStartRoutineIn shall be configured
 DcmDspRoutineSignalLength shall be set to 8
 DcmDspRoutineSignalPos shall be set to 0
 DcmDspStartRoutineOut
 4 paramters with a length of 8 bits shall be configured
 DcmDspRoutineSignalPos shall be set to 0, 8, 16, and 24.
[] ⌈The second one to start and stop the transmission to the diagnose master (31 0x 40 0A):
⌋(DMA_PA_9154)
 DcmDspRoutineFixedLength shall be true
 DcmDspRoutineUsePort shall be true
 Neither input or output parameters are needed
 Start and Stop sub services shall be supported
NvM
The Darh needs 2 NvM blocks to store the event queue and the status of the transmission.
The variable Darh_ErrorQueue shall be mapped to the NvM block:
DarhClassic_IntegrationManual.pdf, Version 5.1.0, Software Platforms Page 8 of 13

*Excerpt: first 8 of 13 pages shown.*
