---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1153_ThirdPartyModules'
description: 'Converted PDF document AN-ISC-8-1153_ThirdPartyModules.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1153_ThirdPartyModules.pdf` (PDF, 627 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 10; title: Third Party Modules; author: Sven Hesselmann

## Converted content

### Page 1

Third Party Modules 
Version 1.0 
2013-07-24 
Application Note AN-ISC-8-1153 
 
 
 
Author(s) Sven Hesselmann 
Restrictions Customer confidential - Vector decides 
Abstract Introduction how to integrate 3rd partly modules into the MICROSAR4 stack 
 
Table of Contents 
 
 1 
Copyright © 2013 - Vector Informatik GmbH 
Contact Information: www.vector.com or +49-711-80 670-0 
1.0 Overview .......................................................................................................................................................... 1 
2.0 Integration in DaVinci Configurator 5 ............................................................................................................... 2 
2.1 Configuration With CFG5 .............................................................................................................................. 2 
2.1.1 Adding of BSWMD File ............................................................................................................................... 2 
2.1.2 Adding a Module to the Current Project ..................................................................................................... 3 
2.2 External Generation Step .............................................................................................................................. 4 
2.2.1 Manual Set-Up ............................................................................................................................................ 5 
2.2.2 Automatic Set-Up ........................................................................................................................................ 5 
2.3 Internal Behavior Description ...............................................................................................................

### Page 2

Third Party Modules 
 
 
 
 2 
Application Note AN-ISC-8-1153 
 
 
Figure 1 – Overview of BSWMD file of MCU 
 
2.0 Integration in DaVinci Configurator 5 
For integration of a module into a MICROSAR stack, different things have to be done. 
If the module fulfills one of the following list points, check this chapter for the description. 
The module: 
• has parts, generated based on the configuration (i.e. ECUC file) 
• requires the SCHM API for Exclusive Area handling 
• has cyclic MainFunction calls 
• needs access to communication PDUs 
 
2.1 Configuration With CFG5 
If the module shall be configured within the CFG5, the tool requires its modules description in a BSWMD file (basis 
software module description). Also the module has to be added to the configuration. 
2.1.1 Adding of BSWMD File 
Provide an additional search path for BSWMD files within your configuration. The BSWMD file must end with 
.arxml to be noticed by CFG5. 
Open Project|Project Setting|Modules|Additional Definitions and Add the path to the module’s BSWMD file as 
shown in the following screenshots.

### Page 3

Third Party Modules 
 
 
 
 3 
Application Note AN-ISC-8-1153 
 
 
Figure 2 – Modules|Additional Definitions 
 
 
Figure 3 – BSWMD added 
 
Now the CFG5 knows the module and it can be added to the configuration. But before the configuration has to be 
closed and opened again. 
2.1.2 Adding a Module to the Current Project 
For adding the module to the current configuration, open Project|Project Settings|Modules and Add it with the 
blue plus. If the path to the module is within the delivered SIP, you will find it in Select from SIP otherwise in 
Select additional definition (see screenshots below).

### Page 4

Third Party Modules 
 
 
 
 4 
Application Note AN-ISC-8-1153 
 
 
Figure 4 – Module Assistant 
 
 
Figure 5 – Module Definitions 
 
Now the module is within your project, configure it using the Basic Editor. 
2.2 External Generation Step 
If the module has parts generated based on the configuration of the ECUC file and the generation shall be started 
from the CFG5, the generation list has to be extended. The configuration of the generation steps for third -party 
modules can either be done manually or by a configuration file, making it easier to reuse your module for further 
projects.

### Page 5

Third Party Modules 
 
 
 
 5 
Application Note AN-ISC-8-1153 
 
2.2.1 Manual Set-Up 
Open Project|Project Settings|Code Generation|External Generation Steps and Add the generation settings 
using the blue plus. 
 
Figure 6 – External Generation Steps 
 
Specify the module generator settings (i.e. parameters to be handed over). If the module generator also supports 
validation or requires a transformation of the input file, this can also be configured. For further information also see 
the Help Content of CFG5. 
2.2.2 Automatic Set-Up 
The settings described in 2.2.1 can also be done automatically by a so-called Settings.xml. For configuration 
options of the Settings.xml please refer to 3.0 Settings.xml. 
2.3 Internal Behavior Description 
Most AUTOSAR modules require Exclusive Area and / or MainFunction handling by the R TE. The MICROSAR 
RTE reads this information from the so-called Internal Behavior description, which is a part of a BSWMD file. This 
file has to be provided to the CFG5 by placing it into the folder for InternalBehavior files (default is 
./Config/InternalBehavior). 
The <BSW-IMPLEMENTATION> container within the BSWMD file must have a reference to the Internal Behavior 
(i.e. <BEHAVIOR-REF DEST="BSW-INTERNAL-
BEHAVIOR">/VendorX/Mcu_ib_bswmd/BswModuleDescriptions/Mcu/McuBehavior</BEHAVIOR-REF>, see also Figure 1). 
The RTE reads the Internal Behavior of the module from this file and provides a solving action to create an 
RteBswModuleInstance with this information. 
2.3.1 Example for Internal Behavior Description 
The following example for an Internal Behavior description defines an exclusive area called MCU_EXCLUSIVE_AREA_0 
and a MainFunction called Mcu_MainFunction, which has to be called with a cycle time of 0.01 seconds. The file 
should be place

### Page 6

Third Party Modules 
 
 
 
 6 
Application Note AN-ISC-8-1153 
 
<?xml version="1.0" encoding="UTF-8" standalone="no"?> 
<AUTOSAR xmlns="http://autosar.org/schema/r4.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://autosar.org/schema/r4.0 autosar_4-0-3.xsd"> 
 <AR-PACKAGES> 
 <AR-PACKAGE> 
 <SHORT-NAME>VendorX</SHORT-NAME> 
 <AR-PACKAGES> 
 <AR-PACKAGE> 
 <SHORT-NAME>Mcu_ib_bswmd</SHORT-NAME> 
 <AR-PACKAGES> 
 <AR-PACKAGE> 
 <SHORT-NAME>BswModuleDescriptions</SHORT-NAME> 
 <ELEMENTS> 
 <BSW-MODULE-DESCRIPTION> 
 <SHORT-NAME>Mcu</SHORT-NAME> 
 <PROVIDED-ENTRYS> 
 <BSW-MODULE-ENTRY-REF-CONDITIONAL> 
 <BSW-MODULE-ENTRY-REF DEST="BSW-MODULE-
ENTRY">/VendorX/Mcu_ib_bswmd/BswModuleDescriptions/Mcu_MainFunction</BSW-MODULE-ENTRY-REF> 
 </BSW-MODULE-ENTRY-REF-CONDITIONAL> 
 </PROVIDED-ENTRYS> 
 <INTERNAL-BEHAVIORS> 
 <BSW-INTERNAL-BEHAVIOR> 
 <SHORT-NAME>McuBehavior</SHORT-NAME> 
 <EXCLUSIVE-AREAS> 
 <EXCLUSIVE-AREA> 
 <SHORT-NAME>MCU_EXCLUSIVE_AREA_0</SHORT-NAME> 
 </EXCLUSIVE-AREA> 
 </EXCLUSIVE-AREAS> 
 <ENTITYS> 
 <BSW-SCHEDULABLE-ENTITY> 
 <SHORT-NAME>Mcu_MainFunction</SHORT-NAME> 
 <IMPLEMENTED-ENTRY-REF DEST="BSW-MODULE-
ENTRY">/VendorX/Mcu_ib_bswmd/BswModuleDescriptions/Mcu_MainFunction</IMPLEMENTED-ENTRY-REF> 
 </BSW-SCHEDULABLE-ENTITY> 
 </ENTITYS> 
 <EVENTS> 
 <BSW-TIMING-EVENT> 
 <SHORT-NAME>Mcu_MainFunctionTimingEvent0</SHORT-NAME> 
 <STARTS-ON-EVENT-REF DEST="BSW-SCHEDULABLE-
ENTITY">/VendorX/Mcu_ib_bswmd/BswModuleDescriptions/Mcu/McuBehavior/Mcu_MainFunction</STARTS-ON-EVENT-REF> 
 <PERIOD>0.01</PERIOD> 
 </BSW-TIMING-EVENT> 
 </EVENTS> 
 </BSW-INTERNAL-BEHAVIOR> 
 </INTERNAL-BEHAVIORS> 
 </BSW-MODULE-DESCRIPTION> 
 <BSW-MODULE-ENTRY> 
 <SHORT-NAME>Mcu_MainFunction</SHORT-NAME> 
 <CALL-TYPE>SCHEDULED</CALL-TYPE> 
 <EXECUTION-CO

### Page 7

Third Party Modules 
 
 
 
 7 
Application Note AN-ISC-8-1153 
 
InternalBehavior folder of your project and adapt them to your configuration (i.e. changing the cycle time of the 
MainFunction). 
2.4 RTE configuration 
If

*Excerpt: first 8 of 10 pages shown.*
