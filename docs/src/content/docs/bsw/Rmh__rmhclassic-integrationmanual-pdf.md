---
title: 'Rmh — RmhClassic_IntegrationManual'
description: 'Converted PDF document RmhClassic_IntegrationManual.pdf from module Rmh.'
sidebar:
  hidden: true
---

> **Source:** `RmhClassic_IntegrationManual.pdf` (PDF, 208 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 11; title: -; author: -

## Converted content

### Page 1

Rmh Classic Integration Manual
Project BMW AUTOSAR 4 Core Rel. 3
Author BMW AG
Release Date 2017-12-14
Version 5.0.0
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
5.0.0 2017-12-14 Initial version for SP2021
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 1 of 11

### Page 2

Table of Contents
1 Introduction 3
1.1 General 3
1.2 Functional overview 3
2 Acronyms and Abbreviations 3
3 Related documentation 4
4 Limitations 5
5 Software Architecture 6
5.1 Dependencies to other Modules 6
5.2 Dependencies to AUTOSAR modules 6
5.2.1 Com 6
5.2.2 RTE 6
5.2.3 Det 6
5.3 Dependencies to other modules 6
6 Integration 7
6.1 Configuration of other modules 7
6.1.1 Com 7
6.1.1.1 ComSignal for Rmh data element requestedMsgID 7
6.1.1.2 Optional ComSignal for Rmh data element dummySignal 7
6.1.2 Det 7
6.2 Configuration 7
6.2.1 Operation Variants of Rmh 7
6.2.1.1 Use zero length dummy trigger signals 7
6.2.1.2 Use direct BSW call to Com_TriggerIPDUSend 8
6.2.2 Rmh General 8
6.2.2.1 RmhDevErrorDetect 9
6.2.2.2 RmhPduTriggerMode 9
6.2.2.3 RmhRequestPduMapping 9
6.3 Configuration of the RTE/SchM 9
6.3.1 Event Mapping 10
6.3.2 Data Mapping 10
6.3.3 Exclusive Areas 10
6.4 Software Integration 10
6.4.1 SWCD Adaption 10
6.4.2 Startup/Initialization 11
6.4.3 Normal Operation 11
6.4.4 Shutdown/Deactivation 11
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 2 of 11

### Page 3

1 Introduction
General
For a general introduction to the BAC4 Platform Modules please refer to [1].
This document only describes topics related to the Rmh BAC4 Module.
This Integration Manual describes the basis functionality, API and the configuration of the BMW system
function Rmh.
Functional overview
The main objective of the Request Message Handler ( Rmh) functionality is to trigger the transmission of
specific Com I-PDUs, when a certain (Com-)Signal is received embedded in a special so-called request
message. The use case in the BMW bordnet is as follows: If certain TX-Pdus of an ECU are marked as
being "requestable" in the bordnet database, the ECU has to support the reception of a specific request
message. In the payload of the request message is defined, which of the ECUs configured requestable
TX-Pdus shall be sent out once again. This feature is used for TX-Pdus, which are either sent out
on-change/on-event only or if the cyclic frequency is very low. Other ECUs in the vehicle, which are
interessted in the reception of such an TX-Pdu can then send a request message to this ECU, to get the
current value instead of waiting for a long time until it is sent out again regularly.
The Rmh module itself is modeled as an AUTOSAR software component (SWC) residing above the RTE.
Depending on the configuration variant an additional CD (complex driver) may be part of the Rmh module.
2 Acronyms and Abbreviations
Abbreviation Acronym: Description:
AUTOSAR Automotive Open Systems Architecture group
BAC BMW AUTOSAR Core
Com AUTOSAR Communication module
Det AUTOSAR Default Error Tracer module
ECU Electronical Control Unit
PDU Protocol Data Unit
Rmh BMW Request Message Handler system function (this module)
RTE Runtime Environment
SWC Software Component
SWCD Software Component De

### Page 4

3 Related documentation
References
[1] BAC4 General Concept for the Module Integration
BAC4_General_Concepts_for_the_Module_Integration.pdf
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 4 of 11

### Page 5

4 Limitations
None.
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 5 of 11

### Page 6

5 Software Architecture
Dependencies to other Modules
The RmhClassic is a standalone module. I.e. there is no generic part of Rmh, since the functionality of
Rmh is only applicable to AUTOSAR CP (Classic AUTOSAR) platform.
Dependencies to AUTOSAR modules
Com
Rmh supports a configuration mode, where it partly takes the role as a complex driver, which directly calls
BSW module Com ( Com_TriggerIPDUSend). In the configuration mode as a pure AUTOSAR SWC it
accesses Com indirectly via Rte_Read/Rte_Write.
RTE
As a software component, the Rmh module uses Rte client/server and sender/receiver communication to
communicate with BSW modules.
Det
Rmh optionally reports development errors to the Det.
Dependencies to other modules
There are no such dependencies.
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 6 of 11

### Page 7

6 Integration
Configuration of other modules
The following modules shall be configured, before the module Rmh is compiled and linked.
Com
ComSignal for Rmh data element requestedMsgID
The ComSignal for the data element requestedMsgID shall be configured. This signal is currently named
ID_FN_INQY in the BMW message catalog and is part of the multiplexed PDU ANFRAGE/Inquiry.
Optional ComSignal for Rmh data element dummySignal
In case the integrator has decided to go for Rmh variant ZERO_LENGTH_SIGNAL (see below), then for
each Com-PDU, that can be requested, a Com dummy trigger signal with ComBitSize 0 and
ComTransferProperty TRIGGERED has to configured and mapped to the corresponding Com-PDU.
Det
Configure the Det accordingly, that it provides the needed P-Port to the Rmh SWC.
Configuration
The Rmh configuration is formally described in cfgdesc/RmhClassic_paramdef.arxml.
Here the configuration values will be set in the right context.
Operation Variants of Rmh
As roughly stated in subsection 6.1.1, ‘‘Com’’ theRmh module can be used in two different modes. These
two modes differ in the mechanism used, how to trigger the transmission of the requested Com-PDU.
The integrator has to decide which variant fits best in his integration scenario.
Use zero length dummy trigger signals
In this variant, the Rmh consists only of one pure AUTOSAR SWC communicating strictly over RTE. To
allow the transmission of a Com-PDU, the following strategy is used: For each PDU, which is configured
as "can be requested", the Rmh module generates an S/R P-Port over which it sends a uint8 dummy data
element. The integrator now has to map each of these data elements to a dummy trigger Com signal,
RmhClassic_IntegrationManual.pdf, Version 5.0.0, Software Platforms Page 7 of 11

### Page 8

which is part of the PDU to be transmitted and which has the property ComTransferProperty set to
TRIGGERED. Since the task of these dummy signals is solely to trigger the PDU transmission and the
content of these signals shall NOT show up in the transmitted PDU on the network, the used Com stack
has to support the concept of zero-length-signals. That means the Com dummy signal must support a
configuration setting ComBitSize with value 0.
Note: This feature is currently marked as optional in AUTOSAR, so you have to check with your stack
vendor, whether he truly supports this.
Pro: This variant does not need any ComplexDeviceDriverSwComponent support. This might be a
benefit in ASIL environments, where the usage of non ASIL qualified ComplexDrivers is critical.
Contra: Depending on the number of PDUs that can be requested in your ECU, the Rmh has an
equivalent number of ports, which consume resources. The additionally needed dummy Com signals also
take up certain resources. Finally the configuration overhead for the integrator (data element mapping to
Com signal mapping, creation of dummy Com signals) may be higher than in variant two.
Use direct BSW call to Com_TriggerIPDUSend
With this Rmh variant, the module consists of two components: An ApplicationSwComponent and a
ComplexDeviceDriverSwComponent. The ComplexDeviceDriverSwComponent is nothing more than a

*Excerpt: first 8 of 11 pages shown.*
