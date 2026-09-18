---
title: 'Crypto — CryptoClassic_IntegrationManual'
description: 'Converted PDF document CryptoClassic_IntegrationManual.pdf from module Crypto.'
sidebar:
  hidden: true
---

> **Source:** `CryptoClassic_IntegrationManual.pdf` (PDF, 132 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 7; title: -; author: -

## Converted content

### Page 1

Crypto Classic Integration Manual
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
5.2.0 2017-12-14 Version Update
5.1.0 2017-11-09 Version Update
5.0.0 2017-10-12 Initial version for SP2021
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 1 of 7

### Page 2

Table of Contents
1 Introduction 3
1.1 Functional overview 3
2 Related documentation 4
3 Limitations 5
4 Software Architecture 6
4.1 Dependencies on AUTOSAR modules 6
4.2 Dependencies to other modules 6
5 Integration 7
5.1 Configuration of other Modules 7
5.2 Configuration 7
5.3 Configuration of the RTE 7
5.4 Key File 7
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 2 of 7

### Page 3

1 Introduction
This Integration Manual describes the basis functionality and the configuration and integration of the
Crypto module.
Functional overview
The main objective of the Crypto functionality is to provide a hardware independant cryptography library
which shall be usable by all BMW ECUs.
The Crypto Module provides the following Crypto primitives :
 SHA-256
 SHA-384
 SHA-512
 ECDSA Signature verification (P-256/P-384/P-521)
 Certificate parsing and signature verification.
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 3 of 7

### Page 4

2 Related documentation
References
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 4 of 7

### Page 5

3 Limitations
No limitations are known.
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 5 of 7

### Page 6

4 Software Architecture
Dependencies on AUTOSAR modules
The current version of the Module Crypto does not depend on any BSW module.
Dependencies to other modules
Crypto includes headers from the BMW BUtil module.
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 6 of 7

### Page 7

5 Integration
Configuration of other Modules
No other module needs to be configured to perform integration of the Crypto library.
Configuration
For a detailed description of the configuration parameters, please consult the description in the Crypto
parameter definition file.
Configuration of the RTE
There are no special requirement for RTE configuration.
Key File
The security key file is generated with BMW backend system SWL-SEC for every ECU. This key file
named Crypto_Keys.h needs to be included directly.
CryptoClassic_IntegrationManual.pdf, Version 5.2.0, Software Platforms Page 7 of 7
