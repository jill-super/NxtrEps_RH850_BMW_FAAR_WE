---
title: 'FrXcp — TechnicalReference_FrXcp'
description: 'Converted PDF document TechnicalReference_FrXcp.pdf from module FrXcp.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_FrXcp.pdf` (PDF, 741 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 37; title: Technical Reference; author: Andreas Herkommer

## Converted content

### Page 1

XCP on FlexRay 
Technical Reference 
 
 
 
 
Version 1.13.00 
 
 
 
 
 
 
 
 
 
 
Status Released

### Page 2

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
1 Document Information 
1.1 History 
Date Version Remarks 
2007-06-11 1.00.00 Creation of document 
2007-07-09 1.01.00 Support of AUTOSAR Memory Mapping 
2007-07-30 1.02.00 New GENy GUI features 
2007-09-10 1.03.00 Update for Vector-Release 
2008-02-25 1.04.00 New Feature “Use Tx Confirmation” 
2009-02-09 1.05.00 Support of Ecuc Import/Export 
2009-09-09 1.06.00 Support a2l export 
2010-08-25 1.07.00 ESCAN00044862: Multiple Transport Layer support 
2010-12-10 1.08.00 ESCAN00046308: AR3-297 AR3-894: Support PduInfoType 
instead of the DataPtr 
2011-08-11 1.09.00 Support of Post Build configuration variant 
2012-11-09 1.10.00 Added Option for AMD Runtime Measurement 
ESCAN00058756 Describe use case for PDU length 
ESCAN00065888 Cluster Name should be Cluster ID 
ESCAN00066648 Describe usage of new Exclusive Areas 
2013-09-10 1.11.00 ESCAN00070207 Optimization - 32bit copy 
ESCAN00070081 Describe resume mode 
ESCAN00069779 Missing description of "Set PduMode Support" 
Feature in GENy 
ESCAN00067440 Max CTO must not be greater than Max DTO 
2014-08-15 1.11.01 ESCAN00077234 AR3-2679: Description BCD-coded return-
value of FrXcp_GetVersionInfo() in TechRef 
2015-05-05 1.12.00 Removed chapter GENy 
ESCAN00083373 Tx Confirmation Timeout Timer 
ESCAN00083375 Missing entries in root config structure 
2016-10-13 1.13.00 ESCAN00092303 FrXcp_Control API replaced by global Variable 
Table 1-1 History of the Document 
1.2 Reference Documents 
Index and Document Name 
[1] XCP -Part 2- Protocol Layer Specification -1.1.pdf 
[2] XCP -Part 3- Transport Layer Specification XCP on FlexRay -1.1.pdf 
[3] API specification of Development Error Tracer, Version 1.0.0 of 2005-07-08 
[4] Specification of Platform T

### Page 3

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
[5] Specification of Standard Types Version 1.0.3 of 2005-12-13 
[6] TechnicalReference_Asr_Xcp.pdf 
Table 1-2 Reference Documents 
1.3 Scope of this document 
This document describes the features, API, configuration and integration of the XCP 
Transport Layer for FlexRay. The XCP Protocol Layer, which is already described within a 
separate document [6], is not covered by this document. 
Please also refer to “The Universal Measurement and Calibration Protocol Family” 
specification by ASAM e.V.

### Page 4

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
Contents 
1 Document Information ................................ ................................ ................................ . 2 
1.1 History ................................ ................................ ................................ ............... 2 
1.2 Reference Documents ................................ ................................ ....................... 2 
1.3 Scope of this document................................ ................................ ...................... 3 
2 Overview ................................ ................................ ................................ ....................... 8 
2.1 Abbreviations and Items ................................ ................................ ..................... 8 
2.2 Naming Conventions ................................ ................................ .......................... 9 
2.3 Architecture Overview ................................ ................................ ........................ 9 
2.3.1 XCP Architecture ................................ ................................ ................ 9 
2.3.2 Detailed Architecture of XCP ................................ ............................ 11 
2.3.3 Include structure ................................ ................................ .............. 11 
3 Functional Description ................................ ................................ ............................... 12 
3.1 Overview of the Functional Scope ................................ ................................ .... 12 
4 Integration into the Application ................................ ................................ ................. 13 
4.1 XCP Transport Layer Files ........

### Page 5

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
5.1 A2L File ................................ ................................ ................................ ............ 19 
5.2 Manual Configuration ................................ ................................ ....................... 19 
5.2.1 Pre-Compile Configuration ................................ ............................... 19 
5.2.2 Link Time & Post Build Configuration ................................ ............... 20 
6 Description of the API ................................ ................................ ................................ 23 
6.1 Data Types ................................ ................................ ................................ ....... 23 
6.2 Global Variables ................................ ................................ ............................... 23 
6.3 Global Constants ................................ ................................ ............................. 23 
6.3.1 Component Versions ................................ ................................ ........ 23 
6.3.2 Vendor ID ................................ ................................ ......................... 23 
6.3.3 Module ID ................................ ................................ ........................ 24 
6.4 Services provided by XCP on FlexRay ................................ ............................. 24 
6.4.1 Administrative Functions ................................ ................................ .. 24 
6.4.1.1 FrXcp_Init: Initialization of XCP on FlexRay ................... 24 
6.4.1.2 FrXcp_MainFunctionRx: Main Function of XCP 
Transport Layer................................ .............................. 24 
6.4.1.3 FrXcp_MainFunct

### Page 6

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
8 Known Issues/ Limitations ................................ ................................ ......................... 35 
8.1 Reconfig LPDU ................................ ................................ ................................ 35 
9 Icons ................................ ................................ ................................ ............................ 36 
10 Contact ................................ ................................ ................................ ........................ 37

### Page 7

Technical Reference XCP on FlexRay 
2016, Vector Informatik GmbH Version: 1.13.00 
Illustrations 
Figure 2-1 XCP Architecture ................................ ................................ ...................... 10 
Figure 2-2 Detailed Architecture of XCP ................................ ................................ .... 11 
Figure 3-1 API of XCP on FlexRay Transport Layer ................................ ................... 12 
Figure 4-1 CANape – PDU relation ................................ ................................ ............ 17 
 
Tables 
Table 1-1 History of the Document ................................ ................................ ............ 2 
Table 1-2 Reference Documents ................................ ................................ ............... 3 
Table 2-1 Abbreviations and Items ................................ ................................ ............ 9 
Table 2-2 Naming Conventions ................................ ................................ ................. 9 
Table 4-1 File List of XCP on FlexRay (object code) ................................ ................ 13 
Table 4-2 File List of XCP on FlexRay (source code)..............................

*Excerpt: first 8 of 37 pages shown.*
