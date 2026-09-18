---
title: 'Srv — IntegrationManual_Srv'
description: 'Converted PDF document IntegrationManual_Srv.pdf from module Srv.'
sidebar:
  hidden: true
---

> **Source:** `IntegrationManual_Srv.pdf` (PDF, 165 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 8; title: -; author: -

## Converted content

### Page 1

Integration Manual Srv
Project BMW AUTOSAR Core 4 Rel. 2
Author BMW AG
Release Date 2015-12-11
Version 3.1.0
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
3.1.0 2015-12-
11
Björn
Sachsenberg
No changes - only version update
3.0.1 2015-03-
13
Björn
Sachsenberg
No changes - only version update
3.0.0 2014-10-
29
Björn
Sachsenberg
Initial version (taken over from BAC4 1.2.x)
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 1 of 8

### Page 2

Table of Contents
1 Introduction 3
1.1 General 3
1.2 Functional overview 3
2 Acronyms and Abbreviations 3
3 Related documentation 4
3.1 BMW Specifications 4
3.2 AUTOSAR Specifications 4
4 Limitations 5
5 Software Architecture 6
5.1 Dependencies on AUTOSAR modules 6
5.2 Dependencies on BMW modules 6
6 Integration 7
6.1 Configuration of other Modules 7
6.2 Configuration 7
6.2.1 General 7
6.2.1.1 HandleEccRam 7
6.2.1.2 HandleEccRom 7
6.2.1.3 MultiCpuEnable 7
6.2.1.4 FeatureSet 7
6.3 Configuration of the RTE 8
6.4 Software Integration 8
6.4.1 Startup/Initialisation 8
6.4.2 Normal Operation 8
6.4.3 Shutdown/Deactivation 8
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 2 of 8

### Page 3

1 Introduction
1.1 General
For a general introduction to the BAC4 Platform Modules please refer to [1].
This document only describes topics related to the SWT BAC4 Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW
system function Srv.
1.2 Functional overview
The Srv (Service) module contains some general purpose functions commonly used by other
modules like Dlog, Prog and Bm. It is used in Application, Bootloader and Bootmanager.
2 Acronyms and Abbreviations
Abbreviation/AcronymDescription
AUTOSAR Automotive Open System Architecture
BAC BMW AUTOSAR Core
ECU Electronic Control Unit
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 3 of 8

### Page 4

3 Related documentation
3.1 BMW Specifications
[1] BAC4 General Concept for the Module Integration
BAC4_General_Concepts_for_the_Module_Integration.pdf
3.2 AUTOSAR Specifications
[2] Specification of Diagnostic Communication Manager
AUTOSAR_SWS_DiagnosticCommunicationManager
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 4 of 8

### Page 5

4 Limitations
No limitations known.
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 5 of 8

### Page 6

5 Software Architecture
5.1 Dependencies on AUTOSAR modules
Dcm
The module Dcm [2] is needed for the type definition Dcm_ProgConditionsType.
5.2 Dependencies on BMW modules
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 6 of 8

### Page 7

6 Integration
6.1 Configuration of other Modules
Nothing to be done here.
6.2 Configuration
The Srv configuration contains the following containers:
 Srv General
6.2.1 General
This container contains the configuration (parameters) of the Srv module. Note that these
configuration parameters also affect the configuration of other modules such as Dlog, Prog, etc.
6.2.1.1 HandleEccRam
This should be enabled if the hardware handles ECC errors in RAM.
6.2.1.2 HandleEccRom
This should be enabled if the hardware handles ECC errors in ROM.
6.2.1.3 MultiCpuEnable
This should be enabled if a multi CPU ECU is used. Note that communication to the slave CPUs
is done via integrator/user defined functions. Please consult the corresponding modules’
integration manuals for details about those functions.
6.2.1.4 FeatureSet
Defines the feature set that will be provided. For SRV_FS_BOOTMANAGER and SRV_FS_BLU
it is reduced to save space in Bootmanager and Blu, respectively. Should be SRV_FS_FULL in
Bootloader and Application.
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 7 of 8

### Page 8

6.3 Configuration of the RTE
No RTE needed.
6.4 Software Integration
6.4.1 Startup/Initialisation
Nothing to be done here.
6.4.2 Normal Operation
Nothing to be done here.
6.4.3 Shutdown/Deactivation
Nothing to be done here.
IntegrationManual_Srv, Version 3.1.0, Platform Software Page 8 of 8
