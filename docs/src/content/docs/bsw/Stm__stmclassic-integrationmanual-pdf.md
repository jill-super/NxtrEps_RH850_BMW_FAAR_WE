---
title: 'Stm — StmClassic_IntegrationManual'
description: 'Converted PDF document StmClassic_IntegrationManual.pdf from module Stm.'
sidebar:
  hidden: true
---

> **Source:** `StmClassic_IntegrationManual.pdf` (PDF, 179 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 14; title: -; author: -

## Converted content

### Page 1

Stm Classic Integration Manual
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
5.2.0 2017-12-14 Initial version for SP2021
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 1 of 14

### Page 2

Table of Contents
1 Introduction 3
1.1 General 3
1.2 Functional overview 3
2 Acronyms and abbreviations 4
3 Related documentation 5
4 Limitations and Known Issues 6
5 Software Architecture 7
5.1 Dependencies on AUTOSAR modules 7
5.1.1 RTE 7
5.1.2 Com 7
5.1.3 Dem 7
5.1.4 BswM 7
5.2 Dependencies to BMW modules 7
6 Integration 8
6.1 Configuration of other Modules 8
6.1.1 Com 8
6.1.2 BswM 8
6.1.3 Dem 9
6.2 Configuration 9
6.2.1 StmGeneral 9
6.3 Configuration of the RTE 11
6.3.1 Assembly connectors 11
6.3.2 Event Mapping 12
6.3.3 Data Mapping 12
6.3.4 Exclusive Areas 13
6.4 Software Integration 13
6.4.1 SWCD 13
6.4.2 Startup/Initialisation 14
6.4.3 Normal Operation 14
6.4.4 Shutdown/Deactivation 14
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 2 of 14

### Page 3

1 Introduction
This Integration Manual describes the basis functionality, API and the configuration and integration of the
BMW System Function Stm.
General
For a general introduction to the BAC4 Platform Modules, please refer to [1].
This document only describes topics related to the Stm BAC4 Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW system
function Stm.
Functional overview
The main objective of the Stm functionality is to supervise signals that are communicated on the system
busses and maintain these states for the local ECU. This means:
This means:
 Make these states available as modes to other software.
 React on some changes of these states (for instance setting Dem enable conditions).
 React on timeouts of these communicated states (set default values, report error events accordingly).
The Stm module itself is modeled as a SWC residing above the RTE.
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 3 of 14

### Page 4

2 Acronyms and abbreviations
Abbreviation
/ Acronym
Description
AUTOSAR Automotive Open Systems Architecture group
BAC BMW AUTOSAR Core
ECU Electronical Control Unit
BswM Basic Software Mode Manager
Com Communication Module
Dem Diagnostic Event Manager
PDU Protocol Data Unit
RTE Runtime Environment
Stm Status Monitoring
SWC Software Component
SWCD Software Component Description
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 4 of 14

### Page 5

3 Related documentation
References
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 5 of 14

### Page 6

4 Limitations and Known Issues
Currently there are no limitations known.
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 6 of 14

### Page 7

5 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Stm Module depends on the following BSW modules:
RTE
As a software component, the Stm module uses RTE client/server communication to communicate with
other SWCs and BSW. Additionally the scheduling is done by the RTE.
Com
According to chapter 1.2 the Stm modules main objective is to monitor certain bus signals. Therefore,
these signals have to be configured in Com and the data element to Com signal mapping has to be
correctly implemented.
Dem
The Stm controls a Dem specific EnableCondition. It uses the Client-Server interface EnableCondition
provided by the Dem.
BswM
The Stm module expects that it will be notified via ModeSwitchEvents, whether the ComSignal for
centralErrorLock can be received or not. The receive ability depends on the state (started/stopped) of the
ComPduGroup the ComSignal is part of. We suggest that the integrator monitors state changes of this
ComPduGroup and notifies these by ModeSwitches with a corresponding rule configuration in the BswM.
Dependencies to BMW modules
Stm does not have dependencies to other modules.
StmClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 7 of 14

### Page 8

6 Integration
Configuration of other Modules
Com
It is optional to configure the following signals in the Com module. In case you disable the corresponding
feature in all configuration variants of container StmFeatureActivation, you do not need to configure the
related ComSignal. Also in cases, you use RTE transformers to serialize network data into data elements
the configuration is done outside of Com.
ComSignal for Stm data element vehicleState
The ComSignal for the data element vehicleState shall be configured. This signal is currently named
ST_CON_VEH in the BMW message catalog and is part of the PDU CON_VEH in CAN and Flexray
configurations. In case of Ethernet configuration it is part of event VehicleCondition of service
VehicleCondition in package BMW.INFRASTRUCTURE. Note: This is a new variant of the vehicle state
information, which starts in the service pack 2015.
ComSignal for Stm data element energyState
The ComSignal for the data element energyState shall be configured. This signal is currently named
ST_ENERG_FZM in the BMW message catalog and is part of the PDU FZZSTD in CAN and Flexray
configurations. In case of Ethernet configuration, it is part of field VehicleStatus (member
statusEnergyFZM) of service StatusEnergy in package BMW.INFRASTRUCTURE. Note: This is a new
variant of the vehicle state information, which starts in the service pack 2015.
ComSignal for Stm data element centralErrorLock
The ComSignal for the data element centralErrorLock shall be configured. This signal is currently named
ST_ILK_ERRM_FZM in the BMW message catalog and is part of the PDU FZZSTD in CAN and Flexray
configurations. In case of Ethernet configuration, it is part of field VehicleStatus (member
statusInterlockErrorMemoryFZM) of service StatusEnergy in package BMW.INFRASTRU

*Excerpt: first 8 of 14 pages shown.*
