---
title: 'Dem — TechnicalReference_Dem'
description: 'Converted PDF document TechnicalReference_Dem.pdf from module Dem.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_Dem.pdf` (PDF, 2076 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 206; title: MICROSAR Diagnostic Event Manager (Dem); author: Thomas Dedler, Alexander Ditte, Matthias Heil, Anna Bosch, Erik Jeglorz, Stefan Hübner, Aswin Vijayamohanan Nair, Savas Ates

## Converted content

### Page 1

MICROSAR Diagnostic Event Manager 
(Dem) 
Technical Reference 
 
 
Version 7.6.1 
 
 
 
 
 
 
 
 
 
 
 
Authors Thomas Dedler, Alexander Ditte, Matthias Heil, Anna Bosch, Erik Jeglorz, 
Stefan Hübner, Aswin Vijayamohanan Nair, Savas Ates 
Status Released

### Page 2

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 2 
based on template version 5.0.0 
Document Information 
History 
Author Date Version Remarks 
A. Ditte 2012-05-04 1.0.0 > Initial Version 
A. Ditte 2012-10-09 1.0.1 > Add chapter 6.2.6.20 and 6.6.1.2.11 
> Add GetEventEnableCondition to chapter 6.6.1.1.2 
M. Heil 2012-11-02 1.1.0 > Architecture Update 
A. Ditte, 
M. Heil 
2013-02-15 1.2.0 > Introduced Measurement and Calibration (chapter 5) 
> Extended chapters 3.4, 3.6, 3.16, 4.3 and 4.3.1 
> Added User Controlled WarningIndicatorRequest 
(chapter 3.17.1) 
> Added chapters 6.2.6.24, 6.2.6.25, 6.6.1.1.9 
M. Heil 2013-04-05 1.3.0 > Support for feature ‘DTC suppression’ 
> Added chapter 3.10, APIs 6.2.6.26 
> Reworked table layout in chapters 4.3, 5.2 
> Reworked Measurement and Calibration (chapter 5) 
> Added measurable items (chapter 5.1) 
M. Heil 2013-06-17 1.4.0 > Added combined events 
> Reworked suppression 
T. Dedler 2013-07-22 1.4.1 > critical section description extended 
T. Dedler, 
M. Heil 
2013-09-04 2.0.0 > Service ID definition changed 
> Post-Build Loadable 
A. Ditte 2013-11-05 2.1.0 > Added OBD DTC and Root cause EventId to chapter 
3.11.2 
> Added limitation for internal data elements in chapter 
8.3 
A. Ditte, 
M. Heil 
2014-01-14 3.0.0 > Added J1939 (chapters 3.20, 6.2.9) 
> Adapted DCM interfaces (chapter 6.2.8) according 
AUTOSAR 4.1.2 
> Added chapter 4.3.1 
> Fixed ESCAN00071673: NvM configuration is not 
described 
> Fixed ESCAN00071511: Missing hint for supported 
feature 'individual post-build loadable' 
> Fixed ESCAN00073677: Incorrect figure for DEM 
initialization states

### Page 3

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 3 
based on template version 5.0.0 
M. Heil 2014-03-27 3.1.0 > Describe deviation in handling operation cycles before 
module initialization. 
> Add dependency to configuration to Dcm APIs. 
> Added warning about time-based de-bouncing and 
maximum fault detection counter in current cycle 
M. Heil 2014-05-08 3.2.0 > Added Event Availability (chapters 3.10.1, 6.2.6.27) 
> Added freeze frame pre-storage (chapters 3.12, 6.2.6.4, 
6.2.6.5) 
> Corrected description of Event and DTC suppression 
(chapters 3.10, 6.2.6.4, 6.2.6.5) 
> Introduced chapter 3.4.4.2 
> Clarified usage of DTC groups (chapter 8.3) 
M. Heil 
A. Ditte 
2014-10-14 4.0.0 > Moved Initialization Pointer (see Dem_PreInit(), 
Dem_Init()) 
> Added API Dem_RequestNvSynchronization() 
> Added de-bounce values in NVRAM and API 
Dem_NvM_InitDebounceData() 
> Added additional aging variant (chapter 3.6), added 
Figure 3-4 
> Added missing configuration variants (chapter 2, 
ESCAN00076237) 
> Added description for NVRAM write frequency (chapter 
3.14.2, ESCAN00078587) 
> Added description for NVRAM recovery (chapter 3.14.3, 
ESCAN00078582) 
> Added support of J1939 nodes 
M. Heil 2015-02-27 4.1.0 > Added APIs, chapters 6.2.6.3, 6.2.6.22 
> Support EnableCondition notification, 3.16.5 
> Added explanation of Dem task mapping, chapter 4.9 
> Added note of reduced queue depth for some events, 
chapter no longer available 
> Updated critical sections, chapter 4.4 
M. Heil 2015-04-20 4.1.1 > Added deviation regarding notification signatures 
(chapters 6.5.1, 8.1) 
> Reworked chapter 3.1 according ESCAN00082555 
M. Heil 2015-06-17 4.2.0 > Extended data callback support (chapters 3.11.3, 
6.5.1.6) 
> Described FDC statis

### Page 4

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 4 
based on template version 5.0.0 
M. Heil 2015-09-14 4.3.0 > More information about NVRam setup (chapter 4.5 ff) 
> Changes due to new option to persist event availability 
(chapters 3.10.1, 6.2.6.27, 6.2.6.13) 
M. Heil 2015-11-26 5.0.0 > Reworked aging behavior, added new behavior (Table 
3-5, Figure 3-4) 
> Clarifications on feature support 
> Fixed ESCAN00086243 (chapter 4.5.1) 
> Fixed ESCAN00086483 (chapter 4.5.2.2) 
M. Heil 2016-01-20 5.0.1 > No changes 
M. Heil 2016-02-03 6.0.0 > Change Dcm notification handling (chapters 3.16.3, 
chapter no longer available) 
> Fixed ESCAN00087584 (chapter 4.5.2) 
> Fixed ESCAN00088862 (chapter 5) 
> Reworked NV write frequency Table 3-8 
> Changed APIs according to RfC72121(chapters 6.2.9.1, 
6.2.9.8) 
> Reworked Autosar deviation Table 3-2 
> Added new header files to Table 4-1 
A. Ditte 2016-04-19 6.0.1 > Added internal data element DEM_OBD_RATIO in 
chapter 3.11.2 
M. Heil 2016-04-22 > Fixed ESCAN00089671 (chapter 4.5) 
M. Heil - 6.1.0 > Version skipped 
A. Bosch 2016-05-04 6.2.0 > Extended number of supported enable and storage 
conditions (chapter 3.8, 3.9) 
> Added API Dem_GetDebouncingOfEvent() 
> Extended EventStatus values for API 
Dem_SetEventStatus() 
> Fixed ESCAN00089498 (Table 3-7 DTC status 
combination) 
M. Heil 2016-07-12 > Explicitly mention that NVRAM needs to be initialized 
after a SW update (chapter 4.5.2.3) 
> Added clarification for combined events to 
DEM_OBD_RATIO in chapter 3.11.2 
A. Bosch 2016-10-25 6.3.0 > Support for S/R callbacks

### Page 5

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 5 
based on template version 5.0.0 
M. Heil 2016-11-15 7.0.0 > MultiCore/MultiPartition support 
> API change to ASR4.3 (chapters 3.4.1 including all 
subchapters, 3.4.2, 3.4.3, 3.4.4, 3.13.2, 3.15, 3.16, 
3.19.1, 3.21, 4.6.3, 6.2.6.1, 6.2.6.8, 6.2.6.9, 6.2.6.18, 
6.2.6.19, 6.2.6.21, 6.2.6.22, 6.2.6.28, 6.2.6.31, 6.2.6.32, 
6.2.6.33, 6.2.7.1, 6.2.8 including all subchapters, 8.1, 
8.3) 
 
A. Bosch 2016-12-15 > Reworked initialization sequence (chapter 3.2) 
> Added and adapted APIs in chapter 6.2 
E. Jeglorz 2017-01-12 > Rework of API Dem_SetEventStatus() and Storage 
Trigger (chapter 3.11.1) due to support of 
DEM_EVENT_STATUS_FDC_THRESHOLD_REACHED 
M. Heil 2017-04-10 7.1.0 > Added ClearDTC notifications (chapters 3.16.6, 
6.5.1.12, 6.6.1.2.13) 
A. Bosch 2017-04-18 7.2.0 > Fixed ESCAN00094549 (chapter 3.16) 
S. Hübner 2017-05-02 > Added TriggerOnMonitorStatus notification 
(chapters 3.16.1, 4.1.2, 6.5.1.13 and Figure 4-1) 
A. Bosch 2017-05-04 > Adapted chapter 3.21 for multiple clients 
A. Nair 2017-05-18 7.3.0 > Rework of API Dem_SetDTCSuppression() 
> Added API Dem_GetDTCSuppression() 
S. Hübner 2017-05-22 > Rework include structure of RTE files in chapters 4.1.2 
and 4.2 
A. Bosch 2017-05-23 > Added API Dem_GetEventStatus() to chapter 6.2.6.8 for 
compatibility reasons. 
E. Jeglorz 2017-06-14 7.4.0 > Added API Dem_GetOperationCycleState() to chapter 
6.2.6.7 
A. Bosch 2017-06-20 > Added healing counters to chapter 3.11.2 
S. Ates 2017-06-21 > Rework of API Dem_SelectDTC() 
S. Hübner 2017-07-03 > Rework argument description and return values of 
ch 6.2.6.18 Dem_GetEventFreezeFrameDataEx() and 
ch 6.2.6.19 Dem_GetEventExtendedDataRecordEx() 
A. Nair 2017-07-04 > Ad

### Page 6

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 6 
based on template version 5.0.0 
A.Nair 2017-08-25 7.6.0 > Updated the list of functions using Exclusive Area 0 
M.Heil 2017-08-30 > Break down the multi partition concept in sub-chapters 
(chapter 3.2) 
M.Heil 2017-09-11 7.6.1 > Fixed ESCAN00096543 (chapters 4.1, 4.2)

### Page 7

Technical Reference MICROSAR Diagnostic Event Manager (Dem) 
© 2017 Vector Informatik GmbH Version 7.6.1 7 
based on template version 5.0.0 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_DiagnosticEventManager.pdf V4.2.0, 
V4.3.0, 
V5.1.0 
[2] AUTOSAR AUTOSAR_SWS_DevelopmentErrorTracer.pdf V3.2.0 
[3] AUTOSAR AUTOSAR_SWS_Diagnosti

*Excerpt: first 8 of 206 pages shown.*
