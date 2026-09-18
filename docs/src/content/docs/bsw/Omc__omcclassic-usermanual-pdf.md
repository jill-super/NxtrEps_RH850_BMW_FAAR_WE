---
title: 'Omc — OmcClassic_UserManual'
description: 'Converted PDF document OmcClassic_UserManual.pdf from module Omc.'
sidebar:
  hidden: true
---

> **Source:** `OmcClassic_UserManual.pdf` (PDF, 149 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 6; title: -; author: -

## Converted content

### Page 1

Omc Classic User Manual
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
5.1.1 2017-10-12 Version Update
5.1.0 2017-08-10 Version Update
5.0.0 2017-06-29 Initial version for SP2021
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 1 of 6

### Page 2

Table of Contents
1 Overview 3
1.1 Purpose 3
2 Related documentation 4
3 API 5
3.1 Datatypes 5
3.1.1 Omc_OperatingModeType 5
3.1.2 Omc_ExtendedOperatingModeType 5
3.2 Interfaces 6
3.2.1 Provided 6
3.2.1.1 OmcOperatingMode 6
3.2.1.2 OmcExtendedOperatingMode 6
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 2 of 6

### Page 3

1 Overview
This User Manual describes the basis functionality, API and the configuration and integration of the BMW
System Function Omc.
Purpose
The main objective of the Omc functionality is to maintain the current Operating Mode of an ECU.
This means:
 Allowing the change of the current Operating Mode via diagnostic request
 Saving the current Operating Mode to Non Volatile RAM (NVRAM)
 Enabling/disabling Dem (more concrete: Setting/Unsetting a enable condition)
 Providing the current Operating Mode to other software components.
The Omc module distinguishes the following vehicle operating modes:
 NORMAL
 ASSEMBLY
 TRANSPORT
 FLASH
Note that in different documents these modes are sometimes called "energy modes" sometimes called
"operating modes". Although both terms are equivalent, we strictly use the term operating mode.
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 3 of 6

### Page 4

2 Related documentation
References
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 4 of 6

### Page 5

3 API
Datatypes
Omc_OperatingModeType
This type is used to represent the Operating Mode.
Type name Omc_OperatingModeType
Type uint8
Values 0x00 OMC_MODE_NORMAL Normal Mode
0x01 OMC_MODE_ASSEMBLY Assembly Mode
0x02 OMC_MODE_TRANSPORT Transport Mode
0x03 OMC_MODE_FLASH Flash Mode
Description Represents the operation mode.
Omc_ExtendedOperatingModeType
This type is used to represent the Extended Operating Mode.
Type name Omc_ExtendedOperatingModeType
Type uint8
Values 0x00 OMC_MODE_EXTENSION_NORMAL Normal Extended Mode
0x01 OMC_MODE_EXTENSION_1 Extended Mode 1
0x02 OMC_MODE_EXTENSION_2 Extended Mode 2
0x03 OMC_MODE_EXTENSION_3 Extended Mode 3
0x04 OMC_MODE_EXTENSION_4 Extended Mode 4
0x05 OMC_MODE_EXTENSION_5 Extended Mode 5
0x06 OMC_MODE_EXTENSION_6 Extended Mode 6
0x07 OMC_MODE_EXTENSION_7 Extended Mode 7
0x08 OMC_MODE_EXTENSION_8 Extended Mode 8
0x09 OMC_MODE_EXTENSION_9 Extended Mode 9
0x0A OMC_MODE_EXTENSION_10 Extended Mode 10
0x0B OMC_MODE_EXTENSION_11 Extended Mode 11
0x0C OMC_MODE_EXTENSION_12 Extended Mode 12
0x0D OMC_MODE_EXTENSION_13 Extended Mode 13
0x0E OMC_MODE_EXTENSION_14 Extended Mode 14
0x0F OMC_MODE_EXTENSION_15 Extended Mode 15
0xFF OMC_MODE_EXTENSION_INVALID Invalid Extended Mode
Description Represents the extended operation mode.
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 5 of 6

### Page 6

Interfaces
Provided
Omc provides two Mode interfaces to the user to be able to detect the current Operating Mode and
Extended Operating Mode. The interface Mode interface, so the user can also trigger able runnable
on-entry, on-change or on-exit of a mode.
OmcOperatingMode
ModeDeclarationGroup OmcOperatingMode {
{
OMC_MODE_ASSEMBLY,
OMC_MODE_BMW_FLASH,
OMC_MODE_NORMAL,
OMC_MODE_TRANSPORT
}
initialMode = OMC_MODE_NORMAL
}
OmcExtendedOperatingMode
ModeDeclarationGroup OmcExtendedOperatingMode {
{
OMC_MODE_EXTENSION_1,
OMC_MODE_EXTENSION_10,
OMC_MODE_EXTENSION_11,
OMC_MODE_EXTENSION_12,
OMC_MODE_EXTENSION_13,
OMC_MODE_EXTENSION_14,
OMC_MODE_EXTENSION_2,
OMC_MODE_EXTENSION_3,
OMC_MODE_EXTENSION_4,
OMC_MODE_EXTENSION_5,
OMC_MODE_EXTENSION_6,
OMC_MODE_EXTENSION_7,
OMC_MODE_EXTENSION_8,
OMC_MODE_EXTENSION_9,
OMC_MODE_EXTENSION_INVALID,
OMC_MODE_EXTENSION_NORMAL,
OMC_MODE_EXTENSION_SAVE_ENERGY
}
initialMode = OMC_MODE_EXTENSION_NORMAL
}
OmcClassic_UserManual.pdf, Version 5.2.0, Software Platforms Page 6 of 6
