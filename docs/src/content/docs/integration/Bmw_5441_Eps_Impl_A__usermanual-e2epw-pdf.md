---
title: '_Bmw_5441_Eps_Impl_A — UserManual_E2EPW'
description: 'Converted PDF document UserManual_E2EPW.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `UserManual_E2EPW.pdf` (PDF, 3673 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 68; title: End-to-End Protection Wrapper Generator; author: -

## Converted content

### Page 1

Schoenbrunner Str. 7, A-1040 Vienna, Austria, Tel. + 43 1 585 34 34-0, Fax +43 1 585 34 34-90, support@tttech-automotiv e.com
The data in this document may not be altered or amended without special notif ication f rom TTTech Automotiv e GmbH. TTTech Automotiv e GmbH
undertakes no f urther obligation in relation to this document. The sof tware described in it can only be used if the customer is in possession of a general
license agreement or single license.
Using and copy ing is only allowed in concurrence with the specif ications stipulated in the contract. Under no circumstances may any part of this
document be copied, reproduced, transmitted, stored in a retriev al sy stem, or translated into another language without written permission of TTTech
Automotiv e GmbH.
The names and designations used in this document are trademarks or brands belonging to the respectiv e owners.
© 2015 TTTech Automotiv e GmbH. All rights reserv ed. Subject to changes and corrections.
TTTech Automotiv e GmbH Conf idential and Proprietary Inf ormation
TTTech Automotive GmbH
2.0.1
13.03.2015
D-MSP-G-70-001
Version:
Date:
Document number:
End-to-End Protection Wrapper Generator
User Manual

### Page 2

End-to-End Protection Wrapper Generator
© 2015 TTTech Automotive GmbH
Document number: D-MSP-G-70-001
Page 2
TTTech Automotive Confidential and Proprietary
End-to-End Protection Wrapper Generator 2.0.1
Table of Contents
1
Introduction
4
................................................................................................................................... 4
1.1
E2E Protection Wrapper Generator
................................................................................................................................... 5
1.2
Tools Integration
................................................................................................................................... 5
1.3
Use Cases
2
Versions
7
3
Installation
7
4
Preprocessor
8
................................................................................................................................... 8
4.1
Preprocessor Help
.......................................................................................................................................................... 8
4.1.1 Using the Preprocessor 
.......................................................................................................................................................... 11
4.1.2 Behavior and Log Output 
.......................................................................................................................................................... 11
4.1.3 Log Message Format 
.......................................................................................................................................................... 12
4.1.4 Warning and Info Log Messages 
5
E2E Protection Wrapper Generator
14
............................................................................................

### Page 3

3
End-to-End Protection Wrapper Generator
© 2015 TTTech Automotive GmbH
Page
Document number: D-MSP-G-70-001 TTTech Automotive Confidential and Proprietary
End-to-End Protection Wrapper Generator 2.0.1
10
Integration Notes
53
................................................................................................................................... 53
10.1
Checking the Tool Input
................................................................................................................................... 53
10.2
Checking the Generated Files
................................................................................................................................... 53
10.3
Performing an Integration Test
.......................................................................................................................................................... 53
10.3.1 Using Restbus Simulation 
......................................................................................................................................................... 55
Example Scenarios
......................................................................................................................................................... 58
Integration Test Message Sequence
......................................................................................................................................................... 63
Hints for Integration Test Setup
.......................................................................................................................................................... 63
10.3.2 Using Intra-ECU Signaling 
...................................................................................................................................

### Page 4

Introduction
Page 4
TTTech Automotive Confidential and Proprietary
© 2015 TTTech Automotive GmbH
End-to-End Protection Wrapper Generator 2.0.1
Document number: D-MSP-G-70-001
1
Introduction
Many automotive applications are distributed among several electronic control units
(ECU) and include communication via embedded networks. The exchanged data is
often critical (for example, car speed or steering angle), and incorrect data could
endanger both, the driver and the car. Therefore, special mechanisms have been
introduced to prevent the processing of incorrect data. One of them is the End-to-End
Communication Protection Library (E2Elib), which has been standardized in
AUTOSAR [AS_E2E_SWS]
.
Most automotive networks protect data with checksums. These mechanisms are not
adequate for protecting the application data, because errors in gateways or software
layers within the ECU could destroy the data before and after it is transferred over the
network. End-to-end protection also covers this path. The E2Elib uses an additional
checksum and a sequence counter in order to detect false and missing data directly in
the application.
The figure below shows an I-PDU with a length of four bytes and a signal with two
bytes:
Byte 1 
Data
Byte 0 Byte 2 Byte 3 
The end-to-end communication protection requires additional signals in the
protected signal area for the checksum and the sequence counter:
Byte 1 
Data
CRC
Seq. counter
Byte 0 Byte 2 Byte 3 
For details about this mechanism, see the AUTOSAR E2Elib Specification
[AS_E2E_SWS]
 and the communication protection specification of the original
equipment manufacturer.
1.1
E2E Protection Wrapper Generator
Applications using the E2Elib or similar communication protection mechanisms have
one major problem: the E2E library protection routines n

### Page 5

5Page
Introduction
TTTech Automotive Confidential and Proprietary
© 2015 TTTech Automotive GmbH
End-to-End Protection Wrapper Generator 2.0.1
Document number: D-MSP-G-70-001
wrapper then builds the I-PDU representation, invokes the E2E library function, and then
the RTE function. For reception, the application calls the wrapper instead of the RTE.
The wrapper receives the DE from the RTE and invokes the E2E library function before
returning the DE.
According to the AUTOSAR E2Elib Specification [AS_E2E_SWS]
, the E2E
Protection Wrapper Generator (E2EPWG) generates the code for the protection
wrapper from a specific E2EConfig file.
Note: This user manual does not cover safety-related topics. For safety-critical projects
that need to fulfill ISO 26262 requirements, refer to the End-to-End Protection Wrapper
Safety Manual [TT_E2EPW_SM]
.
1.2
Tools Integration
This document describes how to use the E2EPWG developed by TTTech Automotive.
Example (integration into the Vector tools environment):
In this environment, a special preprocessor is available. This preprocessor converts the
XML files produced by the Vector tools to a E2EConfig file that can be used as an
input for the E2EPWG.
Vector Tools
XML
Preprocessor
Config
file
E 2 EPW
Generator
. c 
files
. h 
files
developed according to 
ISO 26262 ASIL D
XML
Overview of the E2EPW Gener

*Excerpt: first 8 of 68 pages shown.*
