---
title: 'Vin — UserGuide_Vin'
description: 'Converted PDF document UserGuide_Vin.pdf from module Vin.'
sidebar:
  hidden: true
---

> **Source:** `UserGuide_Vin.pdf` (PDF, 180 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 7; title: -; author: -

## Converted content

### Page 1

User Guide Vin
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
No changes - only version update
3.4.1 2016-08-25 Björn
Sachsenberg
No changes - only version update
3.4.0 2016-03-17 Björn
Sachsenberg
Added section "Getting Notified about a
Changed VIN"
3.3.0 2015-12-11 Björn
Sachsenberg
No changes - only version update
3.2.0 2015-07-10 Björn
Sachsenberg
No changes - only version update
3.1.0 2015-03-13 Björn
Sachsenberg
Added content to section 4.2: "Evaluating the
Qualifier"
3.0.0 2014-10-29 Björn
Sachsenberg
Initial version
UserGuide_Vin, Version 3.5.0, Software Platforms Page 1 of 7

### Page 2

Table of Contents
1 Overview 3
1.1 Purpose 3
2 Acronyms and Abbreviations 3
3 Related documentation 5
3.1 BMW Specifications 5
3.2 AUTOSAR Specifications 5
4 Usage 6
4.1 Receiving the VIN and Qualifier 6
4.2 Evaluating the Qualifier 6
4.3 Getting Notified about a Changed VIN 6
UserGuide_Vin, Version 3.5.0, Software Platforms Page 2 of 7

### Page 3

1 Overview
1.1 Purpose
The Vin module is used to request the VIN over the bus, set the qualifier and hand it over to
application software components.
The Vin module is modeled as an AUTOSAR software component (SWC) residing above the
RTE.
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
CKD Completely Knocked Down. A BMW plant that is not connected to
the central BMW IT.
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
GG Gültigkeitsgruppe
GMT Greenwich Mean Time
HO Handelsorganisation (BMW)
HW Hardware
UserGuide_Vin, Version 3.5.0, Software Platforms Page 3 of 7

### Page 4

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
SWT SWEEPING Technologies (SoftWare Enabled Electronic Platform for
Innovative Next Generation Technologies)
UDS Universal Diagnostic Services
UI Upgrade Index
UTC Coordinated Universal Time
VCM Vehicle Configuration Management
VIN Vehicle Identification Number
VIN7 The last 7 digits of the 17-digit VIN
All abbreviations used throughout this document -- except the ones listed here -- can be found
in the official AUTOSAR glossary [1].
UserGuide_Vin, Version 3.5.0, Software Platforms Page 4 of 7

### Page 5

3 Related documentation
3.1 BMW Specifications
3.2 AUTOSAR Specifications
[1] Glossary
AUTOSAR_TR_Glossary
UserGuide_Vin, Version 3.5.0, Software Platforms Page 5 of 7

### Page 6

4 Usage
This section describes all functional Vin features to be used by an application.
4.1 Receiving the VIN and Qualifier
1 Vin_VinType ExternalVIN;
2
3 if( E_OK == Rte_Read_Vin_Vin_Vin(&ExternalVIN))
4 {
5 /* ExternalVIN.Vin contains the VIN,
6 ExternalVIN.Qualifier contains the corresponding qualifier */
7 }
4.2 Evaluating the Qualifier
There is a macro to easily evaluate the qualifier in Vin_Helper.h. The check, whether an
external VIN has been received at all, use the following code snipped:
1 #include "Vin_Helper.h"
2
3 if (VIN_CHECKQUALIFIER(ExternalVIN.Qualifier, VIN_CQ_VIN_RECEIVED))
4 {
5 /* An external VIN has been received */
6 }
To check for a verified secure VIN, use
1 #include "Vin_Helper.h"
2
3 if (VIN_CHECKQUALIFIER(ExternalVIN.Qualifier, VIN_CQ_VIN_SECURE))
4 {
5 /* An external secured VIN has been received and verified */
6 }
For a plain VIN in an unsafe environment, use the same with VIN_CQ_VIN_UNSAFE.
4.3 Getting Notified about a Changed VIN
If a received VIN is different from the last received VIN, the mode VinChangeIndicator is
switched to VIN_CI_CHANGED.
The mode will stay in VIN_CI_CHANGED until shutdown of the ECU. On the next start-up, the
mode will switch to VIN_CI_NOCHANGE if the same VIN is received.
Hint: If you need to trigger a long-running operation on a VIN change, you should write a flag
into NVM in your ON-ENTER Runnable and then trigger the operation. So if the ECU shuts down
UserGuide_Vin, Version 3.5.0, Software Platforms Page 6 of 7

### Page 7

before the long-running operation has finished, you can restart it in the next life cycle according
to the flag.
UserGuide_Vin, Version 3.5.0, Software Platforms Page 7 of 7
