---
title: 'SysTime — SysTimeClassic_IntegrationManual'
description: 'Converted PDF document SysTimeClassic_IntegrationManual.pdf from module SysTime.'
sidebar:
  hidden: true
---

> **Source:** `SysTimeClassic_IntegrationManual.pdf` (PDF, 227 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 11; title: -; author: -

## Converted content

### Page 1

SysTime Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.0.3
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
5.0.3 2017-12-14 Version Update
5.0.2 2017-10-12 Version Update
5.0.1 2017-08-10 Version update, no change of content.
5.0.0 2017-06-08 Initial version for SP2021
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 1 of 11

### Page 2

Table of Contents
1 Introduction 3
1.1 Functional overview 3
2 Related documentation 4
3 Limitations 5
4 Software Architecture 6
4.1 Dependencies on AUTOSAR modules 6
4.1.1 RTE 6
4.1.2 Det 6
4.1.3 Dcm 6
4.1.4 Dem 6
4.1.5 Com 6
4.1.6 BswM 6
4.2 Dependencies to other modules 6
5 Integration 7
5.1 Configuration of other Modules 7
5.1.1 Dcm 7
5.1.2 Com 7
5.1.3 Dem 7
5.1.4 BswM 8
5.1.5 Det 8
5.2 Configuration of generic part 8
5.2.1 SysTimeGeneral 8
5.2.1.1 SysTimeDevErrorDetect 8
5.2.1.2 SysTimeMainTaskCycle 9
5.2.1.3 SysTimeInitialTimeout 9
5.3 Configuration of adapter part 9
5.3.1 SysTimeGeneral 9
5.3.1.1 SysTimeEnableServiceInterface 9
5.4 Configuration of the RTE 9
5.4.1 Assembly Software Connectors 9
5.4.1.1 Dcm 10
5.4.1.2 Dem 10
5.4.1.3 Det 10
5.4.1.4 BswM 10
5.4.1.5 Other Application SWC 10
5.4.2 Event Mapping 10
5.4.3 Data Mapping 10
5.4.4 Exclusive Areas 11
5.5 Software Integration 11
5.5.1 Startup/Initialization 11
5.5.2 Normal Operation 11
5.5.3 Shutdown/Deactivation 11
5.5.4 SWCD 11
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 2 of 11

### Page 3

1 Introduction
This Integration Manual describes the basic functionality of the BMW system function "System Time
Client", the configuration of the SysTime module and of dependant modules, and the integration of the
SysTime module into the BAC4.
[IM_SysTime_0001] ⌈The SysTime module shall be integrated in every diagnosable ECU.
⌋(DMA_PA_9033)
Functional overview
The system time represents the time, which has passed since the initialization of the System Time
Master. The main objective of the System Time Client functionality is to maintain the current system time
for the local ECU. This means:
 Receiving the system time from the System Time Master
 Interpolation of the system time if no system time signal was received from the System Time Master
 Providing the system time to the Dem and to other software components
 Providing the system time for diagnostic requests
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 3 of 11

### Page 4

2 Related documentation
References
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 4 of 11

### Page 5

3 Limitations
No limitations are known.
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 5 of 11

### Page 6

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module SysTime depends on the following BSW modules:
RTE
As a software component, the SysTime module uses Rte client/server communication as well as
sender/receiver communication to communicate with other SWCs and BSW modules. Additionally the
scheduling is done by the Rte.
Det
The System Time Client optionally reports development errors to the Det.
Dcm
The System Time Client implements a ReadDataByIdentifier service. Dcm shall be configured in a way,
that it dispatches the job 0x22 0x17 0x01 to the SysTime SWC.
Dem
The System Time Client provides a port interface for the Dem to get the current system time, which will
be attached to an event as event related data.
Com
The System Time Client receives the signal containing the current system time from the Com module.
BswM
The System Time Client receives and requests mode switches from the BswM.
Dependencies to other modules
SysTime does not have dependencies to other modules.
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 6 of 11

### Page 7

5 Integration
Configuration of other Modules
The following modules shall be configured, before this module can be generated, compiled and linked.
Dcm
[IM_SysTimeClassic_0003] ⌈The ReadDataByIdentifier request 0x22 0x17 0x01 shall be configured
in the Dcm module with the following settings:
 a container "DcmDspData" with
 a "DcmDspDataSize" of 32 bit (4 bytes)
 "DcmDspDataType" =
UINT8N ”DcmDspDataU seP ort” = U SE_DAT A_SY N CH _CLIEN T _SERV ER
 "DcmDspDataConditionCheckReadFncUsed" = FALSE
 a container "DcmDspDid" with
 "DcmDspDidIdentifier" = 0x1701
 only read-access, without session or security restrictions
 one DID Signal "DcmDspDidSignal" with Data Position = 0 and a Data Reference to the
"DcmDspData" container configured before.
⌋(DMA_PA_8550, DMA_PA_8551, DMA_PA_8552)
Com
In the Com module, a signal has to be configured, that receives the message containing the 32-bit
system time from the bus.
Note: In a Can or FlexRay environment, the system time is received within the signal named
T_SEC_COU_REL. In an Ethernet environment, the system time is received within the Parameter
"timeSecondCounterRelative" of the Event "RelativeTimeBN2020".
Dem
[IM_SysTimeClassic_0006] ⌈To attach the system time to a freeze frame of a Dem entry, the
following has to be configured in the Dem module:
 a Data Element Class "DemDataElementClass"
 of type "DemExternalCSDataElementClass"
 with a size "DemDataElementDataSize" of 4 byte
 with port usage "DemDataElementUsePort" = TRUE
 a Data Id "DemDidClass" with reference to the Data Element Class mentioned above
 with reference to the Data Element Class mentioned above
 with "DemDidIdentifier" = 0x1701
SysTimeClassic_IntegrationManual.pdf, Version 5.0.3, Software Platforms Page 7 of 11

### Page 8

 a Freeze Frame Class "DemFreezeFrameClass" with reference to the Data Id above
This DemFreezeFrameClass has to be referenced in the "DemDTCAttributes" of every DTC.
⌋(DK_T3_1374, DK_T3_452, DK_T3_453)
BswM
The BswM has to provide one BswMModeRequestPort to receive mode switches of the
ModeDeclarationGroup "SysTime_LifeCycle" from the SysTime module, and one RteModeRequestPort
to request modes of the ModeDeclarationGroup "SysTime_LifeCycle".
To initialize the SysTime module the BswM has to provide a rule, that results in an action that requests
the mode "SYSTIME_INITIALIZED"of the mode declaration group "SysTime_LifeCycle".
To set the SysTime module to normal operation mode the BswM has to provide a rule, that results in an
action that requests the mode "SYSTIME_RUNNING" of the mode declaration group
"SysTime_LifeCycle". This rule shall be triggered, if the mode has been switched to
"SYSTIME_INITIALIZED" by the SysTime module itself, AND it is technically possible to receive the
system time on the bus. When the SysTime module is in normal operation mode, the SysTime module
switches the mode to "SYSTIME_RUNNING".
To deactivate the SysTime module the BswM has to provide a rule, that results in an action that requests
the mode "SYSTIME_STOPPED" of the mode declaration group "SysTime_LifeCycle".
For details on how to initialize / deactivate the SysTime module, please refer to chapter 6.4.
Det
A SysTime entry shall be added to the Software Component List from Det. This is only necessary, if the
parameter "SysTimeDevErrorDetect" is set to "true" (see chapter 6.2).
Configuration of generic part
SysTimeGeneral
This container contains the configuration parameters of the generic part of the SysTime module
SysTimeDevErrorDetect
This parameter activates/deactivates the Development

*Excerpt: first 8 of 11 pages shown.*
