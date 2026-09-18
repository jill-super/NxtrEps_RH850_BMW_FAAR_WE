---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_Rte'
description: 'Converted PDF document TechnicalReference_Rte.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Rte.pdf` (PDF, 2290 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 145; title: MICROSAR RTE; author: PES1.3

## Converted content

### Page 1

MICROSAR RTE 
Technical Reference 
 
 
Version 4.16.0 
 
 
 
 
 
 
 
 
 
 
Author PES1.3 
Status Released

### Page 2

Technical Reference MICROSAR RTE 
© 2017 Vector Informatik GmbH Version 4.16.0 2 
based on template version 3.5 
Document Information 
History 
Author Date Version Remarks 
Bernd Sigle 2005-11-14 2.0.0 Document completely reworked and adapted to 
AUTOSAR RTE 
Bernd Sigle 2006-04-20 2.0.1 API description for Rte_IRead / Rte_IWrite added, 
description of used OS/COM services added 
Bernd Sigle 2006-07-11 2.0.2 API description for Rte_Receive / Rte_Send added; 
Adaptation to RTE SWS 1.0.0 Final 
Martin Schlodder 2006-11-02 2.0.3 Separation of RTE and target package 
Martin Schlodder 2006-11-15 2.0.4 Client/Server communication 
Martin Schlodder 2006-12-21 2.0.5 Serialized client/server communication 
Martin Schlodder 2007-01-17 2.0.6 Array data types 
Martin Schlodder 2007-02-14 2.0.7 Added exclusive areas, removed description of 
TargetPackages 
Bernd Sigle 2007-02-19 2.0.8 Added transmission acknowledgement handling and 
minor rework of the document 
Bernd Sigle 2007-04-25 2.0.9 Added Rte_IStatus 
Martin Schlodder 2007-04-27 2.0.10 Added IRV and Const/Enum 
Martin Schlodder 
Bernd Sigle 
2007-05-01 2.1.0 Completed documentation for Version 2.2 
Bernd Sigle 2007-07-27 2.1.1 Added Rte_InitMemory, Rte_IWriteRef Runnable. 
Added description of runnable activation offset und 
updated picture of MICROSAR architecture. 
Martin Schlodder 2007-08-03 2.1.2 Added description of template update. 
Martin Schlodder 
Bernd Sigle 
2007-11-16 2.1.3 Added warning regarding IWrite / IrvIWrite. 
Added API descriptions of VFB trace hooks. 
Updated data type info for nested types. 
Martin Schlodder 
Bernd Sigle 
2008-02-06 2.1.4 Updated descriptions on template merging and task 
mapping. 
Added description of Rte_Pim, Rte_CData, 
Rte_Calprm and Rte_Result. 
Added support of string data type. 

### Page 3

Technical Reference MICROSAR RTE 
© 2017 Vector Informatik GmbH Version 4.16.0 3 
based on template version 3.5 
Bernd Sigle 2008-04-16 2.3.0 Added description about A2L file generation and 
updated command line options and example calls to 
cover also the AUTOSAR XML input files. 
Bernd Sigle 2008-07-16 2.4.0 Removed limitations for multiple instantiation and 
compatibility mode support. 
Bernd Sigle 2008-08-13 2.5.0 Added description of indirect APIs Rte_Port, Rte_Ports 
and Rte_NPorts. Added description of platform 
dependent resource calculation. 
Bernd Sigle 2008-10-23 2.6.0 Added description of memory protection support. 
Bernd Sigle 2009-01-23 2.7.0 Added description of mode management APIs 
Rte_Mode and Rte_Switch and updated description of 
Rte_Feedback. 
Added description of Rte_Invalidate and 
Rte_IInvalidate and added new Com APIs. 
Added additional runnable trigger events and removed 
section for runnables without trigger, which is no 
longer supported. 
Deviation for [rte_sws_2648] added. 
Usage of new document template 
Bernd Sigle 2009-03-26 2.8.0 Removed limitations for unconnected ports and for 
data type generation. 
Sascha Sommer 
Bernd Sigle 
2009-08-11 2.9.0 Added description about usage of basic / extended 
task 
Added description of command line parameter -v 
Sascha Sommer 
Bernd Sigle 
2009-10-22 2.10.0 Added a warning for VFB trace hooks that prevent 
macro optimizations 
Explained that the Activation task attribute has to be 
set for basic tasks 
Init-Runnables no longer need to have a special suffix 
Explained the new periodic trigger implementation 
dialog. 
Server runnables with CanBeInvokedConcurrently set 
to false do not need to be mapped to tasks when the 
calling clients cannot interrupt each other 
Resource Usage is now listed in a HT

### Page 4

Technical Reference MICROSAR RTE 
© 2017 Vector Informatik GmbH Version 4.16.0 4 
based on template version 3.5 
Bernd Sigle 
Sascha Sommer 
2010-05-26 2.12.0 Added new measurement chapter, added description 
of COM Rx Filter, macros for access of invalid value, 
initial value, lower and upper limit, added support of 
minimum start interval and second array passing 
variant. Support of AUTOSAR Release 3.1 (RTE SWS 
2.2.0) 
Bernd Sigle 
 
2010-07-22 2.13.0 Added online calibration support. Removed limitation 
of missing transmission error detection 
Bernd Sigle 
 
2010-09-28 2.13.1 Added more detailed description of extended record 
data type compatibility rule 
Bernd Sigle 
 
2010-11-23 2.14.0 Removed obsolete command line parameters –bo, –bc 
and –bn. 
Stephanie Schaaf 
Bernd Sigle 
Sascha Sommer 
2011-07-25 2.15.0 Added general support of AUTOSAR Release 3.2.1 
(RTE SWS 2.4.0). 
Added support of never received status. 
Added support of S/R update handling. 
Mentioned that –g c and –g i ignore service 
components when –m specifies an ECU project. 
Explained RTE usage with Non-Trusted BSW 
Added hint for FUNC_P2CONST() problems 
Explained measurement of COM signals 
Stephanie Schaaf 
Bernd Sigle 
Sascha Sommer 
2012-01-25 2.16.0 Enhanced command line interface (support for several 
generation modes in one command line call, optional 
command line parameter –m) 
Split of RTE into OS Application specific files 
Byte arrays no longer need to be mapped to signals 
groups 
Allow configuration of Schedule() calls in non-
preemptive tasks 
Bernd Sigle 2012-05-18 2.17.0 Corrected description how the Rte_IsUpdated API can 
be enabled 
Bernd Sigle 2012-09-18 2.18.0 Added general support of AUTOSAR Release 3.2.2 
(RTE SWS 2.5.0). 
Added support of non-queued N:1 S/R communication 

### Page 5

Technical Reference MICROSAR RTE 
© 2017 Vector Informatik GmbH Version 4.16.0 5 
based on template version 3.5 
Katharina Benkert 
Stephanie Schaaf 
Sascha Sommer 
Bernd Sigle 
2013-10-30 4.2.0 Added support for arrays of dynamic data length 
(Rte_Send/Rte_Receive) 
Added support for parallel generation for multiple 
component types 
Multicore support 
Added support for SchM Contract Phase Generation 
Added support for Nv Block SWCs 
Katharina Benkert 
Sascha Sommer 
Stephanie Schaaf 
2014-02-06 4.3.0 Added support of VFB Trace Client Prefixes 
Optimized Multicore support without IOCs 
Memory Protection support for Multicore systems 
Inter-ECU sender/receiver communication, queued 
sender/receiver communication and mapped 
client/server calls are no longer limited to the BSW 
partition 
Added support of Development Error Reporting 
Added support of registering XCP Events in the XCP 
module configuration 
Stephanie Schaaf 
Bernd Sigle 
2014-06-17 4.4.0 Support for unconnected client ports for synchronous 
C/S communication 
Inter-Ecu C/S communication using SOME/IP 
Transformer 
Support for PR-Ports 
S/R Serialization using SOME/IP Transformer and E2E 
Transformer 
Support LdCom 
Bernd Sigle 2014-08-13 4.4.1 Described decimal coding of the version defines and 
the return code of SchM_GetVersionInfo 
Added chapter about additional copyrights of FOSS 
Bernd Sigle 2014-09-12 4.4.2 Minor format changes only 
Bernd Sigle 2014-08-13 4.5.0 Support Postbuild-Selectable for variant data 
mappings and variant COM signals 
Support E2E Transformer for Inter-Ecu C/S 
communication 
Support tasks mappings where multiple runnable or 
schedulable entities using different cycle times or 
activation offsets are mapped to a single Basic Task. 
The realization uses OS Schedule Tables 
Supp

### Page 6

Technical Reference MICROSAR RTE 
© 2017 Vector Informatik GmbH Version 4.16.0 6 
based on template version 3.5 
Bernd Sigle 2014-12-08 4.6.0 Support of PR Mode Ports 
Support of PR Nv Ports 
Support of bit field data types (CompuMethods with 
category BITFIELD_TEXTTABLE) 
Runtime optimized copying of large data 
Support for SW-ADDR-METHOD on RAM blocks of 
NvRAM SWCs 
Bernd Sigle 2015-02-20 4.7.0 Support of background triggers 
Support of data prototype mappings 
Support of bit field text table mappings 
Support of union data types 
Support of UTF16 data type serialization in the 
SOME/IP transformer 
Run

*Excerpt: first 8 of 145 pages shown.*
