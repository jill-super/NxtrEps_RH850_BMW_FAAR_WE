---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1208_DaVinciTeamAndPlatformSupport'
description: 'Converted PDF document AN-ISC-8-1208_DaVinciTeamAndPlatformSupport.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1208_DaVinciTeamAndPlatformSupport.pdf` (PDF, 851 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 19; title: DaVinci Team and Platform Support; author: Wernicke, Matthias

## Converted content

### Page 1

DaVinci Team and Platform Support 
Version 1.0 .1 
2017- 09- 06 
Application Note AN-ISC -8-1208 
Author Wernicke, Matthias 
Restrictions Customer Confidential – Vector decides 
Abstract This application note describes how to organize DaVinci projects optimally for 
development with large teams. 
 
 
Table of Contents 
1 Overview ........................................................................................................................................ 2 
1.1 Abbreviations ....................................................................................................................... 2 
2 Background ................................................................................................................................... 2 
2.1 Collaboration (multi-user) ..................................................................................................... 2 
2.2 Product Line Approach ........................................................................................................ 3 
3 Diff and Merge ............................................................................................................................... 4 
3.1 Concepts .............................................................................................................................. 4 
3.2 Project Merge ....................................................................................................................... 5 
3.3 Merge Approaches (2-way, 3-way) ...................................................................................... 5 
3.4 Object Identification ............................................................................................................. 7 
3.5 Project Merge in a Multi-User Development Process ..................

### Page 2

DaVinci Team and Platform Support 
Copyright © 2017 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Overview 
This application note describes how to organize DaVinci projects and how to use the DaVinci tool 
features optimally to 
> Enable collaborative development of a project with a team of developers 
> Enable a product line approach 
It covers aspects of 
> Configuration management 
> Management of libraries of AUTOSAR models (SWCs, EcuC) 
> Diff and merge of AUTOSAR models 
> Platform development support 
Required tool versions: 
> DaVinci Configurator Pro 5.16 or later 
> DaVinci Developer 4.1 or later 
1.1 Abbreviations 
Term Meaning 
CM Configuration Management 
DEV DaVinci Developer 
CFG PRO DaVinci Configurator Pro 
SDG Special Data Group 
UUID Universally Unique Identifier 
ARXML AUTOSAR XML 
SWC Software Component 
ECUC ECU Configuration 
DCF DaVinci Configuration File 
SIP Software Integration Package 
SVN Subversion 
 
 
2 Background 
AUTOSAR ECU SW is typically developed by a project team of several, sometimes dozens of team 
members. To organize the work, following approaches are typically used 
> Collaboration 
> Product Line Approach 
These approaches also have to be applied to the DaVinci projects. 
2.1 Collaboration (multi-user) 
Several project members work on the same SWC or the same BSW module. Parallel working must be 
possible. Reserved editing of the DaVinci project by one user is normally not accepted since it blocks 
the other users.

### Page 3

DaVinci Team and Platform Support 
Copyright © 2017 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Figure 1 - Collaboration 
The DaVinci tools support collaboration with following concepts 
> Diff and Merge, see section 3 
> Configuration management, see section 6 
2.2 Product Line Approach 
A TIER1 typically offers an ECU product to several OEMs. The common parts for all OEM projects are 
developmed within a platform project. The OEM-specific projects are derived from this platform 
project. 
Furthermore, several ECU products may share a common library of AUTOSAR artifacts, e.g. standard 
data types, compu methods, etc. 
 
 
Figure 2 – Product Line Approach 
Over the time, the SW functionality of the ECU is developed as shown in Figure 3:

### Page 4

DaVinci Team and Platform Support 
Copyright © 2017 - Vector Informatik GmbH 4 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Figure 3 – Development process with a platform and several projects 
A platform team is mainly responsible for developing the central ECU functions F1, F2, F3 that make 
the product and are relevant for all OEMs. The goal is to provide a common set of integrated functions 
consisting of SWCs and matching BSW configuration. 
With an independent time schedule, individual OEM project teams derive their project from the 
platform, and may develop OEM-specific functions F4 (OEM A) and F5 (OEM B). To benefit from the 
development of the platform team, the OEM projects are later on updated to the latest version of the 
platform. This update process shall happen under control of the project team. It shall only affect those 
functions, which have been taken over from the platform. The OEM-specific functions shall not be 
touched. 
The DaVinci tools support the product line approach with following concepts 
> Platform functions, see section 4 
> Library mechanisms, see section 5 
Note: We assume that the BSW configuration cannot be completely derived from the SWCs, even if 
they are equipped with service needs. There is always an authoring step required to complete the 
BSW configuration. Therefore, it is not sufficient to just take over the SWCs and assume that the BSW 
configuration can be automatically completed in a deterministic way. 
3 Diff and Merge 
3.1 Concepts 
A simple solution for team collaboration would be the attempt to place the DaVinci project folder on a 
shared drive, where several persons remotely access the same project folder. This will lead to race 
conditions and uncontrolled changes with a high risk of inconsistencies 

### Page 5

DaVinci Team and Platform Support 
Copyright © 2017 - Vector Informatik GmbH 5 
Contact Information: www.vector.com or +49-711-80 670-0 
3.2 Project Merge 
The merge of a DaVinci project is controlled via an according project merge function of CFG PR O 
> Load the MINE project 
> Select the OTHER project 
The AUTOSAR model inside this project will not be changed. 
> Optional: Select the BASE project 
The AUTOSAR model inside this project will not be changed. 
> Launch DEV to merge the SWCs inside the DCF workspace. 
Save the DCF workspace when done. After saving, CFG PRO will automatically resynch. 
> Continue with CFG PRO to merge the ECUC 
Save the project when done. 
 
 
Figure 4 - Project Merge Workflow 
 
 
Note 
Do not try to merge service SWCs with DEV – like BswM, Dem etc. or other SWCs 
generated by CFG PRO. This happens indirectly by merging according module 
configuration with CFG PRO. 
 
3.3 Merge Approaches (2-way, 3-way) 
The two-way merge is applied when importing any ARXML files or when merging two DaVinci 
projects that have no common ancestor. The loaded project (MINE) is compared to the imported 
model (OTHER). Differences are displayed like from the perspective of MINE: 
> Added (exists in OTHER but not in MINE) 
> Removed (exists in MINE but not in OTHER) 
> Modified (exists in both MINE and OTHER, but is not identical) 
Merge decisions have to be met by the user.

### Page 6

DaVinci Team and Platform Support 
Copyright © 2017 - Vector Informatik GmbH 6 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Figure 5 - Two-way Merge 
In the example in Figure 5 the differences are 
> Modified: size of DataType1 
> Removed: SWC2 
The three-way merge is applied when merging two DaVinci projects that have a common ancestor. 
The loaded project (MINE) is compared to the imported model (OTHER) and the common ancestor 
(BASE). Differences are displayed like 
> Removed in MINE 
> Added in MINE 
> Changed in MINE 
> Removed in OTHER 
> Added in OTHER 
> Changed in OTH

*Excerpt: first 8 of 19 pages shown.*
