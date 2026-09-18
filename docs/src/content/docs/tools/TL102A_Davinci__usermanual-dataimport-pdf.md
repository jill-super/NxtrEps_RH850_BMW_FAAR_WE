---
title: 'TL102A_Davinci — UserManual_DataImport'
description: 'Converted PDF document UserManual_DataImport.pdf from module TL102A_Davinci.'
sidebar:
  hidden: true
---

> **Source:** `UserManual_DataImport.pdf` (PDF, 119 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 12; title: Microsoft Word - UserManual_DataImport.doc; author: viswk

## Converted content

### Page 1

Data Import 
User Manual 
 
 
 
 
Version 2.0 
 
 
 
 
 
 
Authors: Matthias Wernicke 
Version: 2.0 
Status: released (in preparation/completed/inspected/released)

### Page 2

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
1 History 
Author Date Version Remarks 
Wk 2009-08-27 1.0 Initial version 
Wk 2011-01-07 2.0 
Document scope extended: description of 
general import mechanisms, description of 
special import functions completed 
 
Contents 
1 History....................................................................................................................... 2 
2 About this Document ............................................................................................... 3 
3 Use Cases ................................................................................................................. 4 
4 Approach .................................................................................................................. 6 
4.1 Definition of import mode via difference analysis ........................................ 7 
4.2 Interactive definition of import mode ........................................................... 8 
4.3 Preset of import mode (automatic merge)................................................... 8 
4.3.1 Preparation of workspace........................................................................... 8 
4.3.2 Automatic pre-setting of import mode for new imported objects.................. 9 
4.3.3 Resulting behavior of DaVinci Developer.................................................... 9 
5 Special Import Functions......................................................................................... 9 
5.1 Overwrite Import Mode Preset.................................................................. 10 
5.2 Update Diagnostic Configuration .............................................................. 11 
6 Contact..........................................................

### Page 3

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
2 About this Document 
This document describes the specific features of DaVinci Developer for importing data 
according to the AUTOSAR SWC Template. It is applicable for the import of AUTOSAR 
XML files or DCF files (DaVinci Configuration File). 
For details about the import function for the ECU Configuration Template, please see 
TechnicalReference_EcuConfigurationFiles.pdf. 
Abbreviations and Items used in this Document: 
SWC Software Component 
PIM Per-Instance Memory

### Page 4

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
3 Use Cases 
The specific import/update features of DaVinci Developer are relevant for scenarios, where 
several involved persons (e.g. the OEM and the TIER1) both contribute SWC design 
artifacts to the overall project. 
 
Figure 1 shows an example, where the TIER1 needs to integrate a SWC of the OEM 
 
/square6 OEM defines an atomic component type with some port prototypes (A). OEM exports 
the component type and passes it to the TIER1 
/square6 TIER1 imports the component type, and integrates it as component prototype into a 
composition type, which already has some other component prototypes and port 
prototypes (red color in B). 
/square6 OEM changes the atomic component type, e.g. by adding some port prototypes and 
removing others (C). OEM exports the component type and passes it to the TIER1 
/square6 TIER1 imports the component type, and expects that the changes of the OEM are 
incorporated (D)

### Page 5

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
SWC2 
Composition1 
SWC1 
SWC2 
SWC2 
Composition1 
SWC1 
SWC2 
OEM Workspace TIER1 Workspace 
A B
C D 
Figure 1: Import/Update Example 1 
 
 
 
 
Figure 2 shows an example, where the TIER1 needs to extend a composition of the OEM 
 
/square6 OEM defines a composition type with some port prototypes and component 
prototypes (A). OEM exports the composition type and passes it to the TIER1 
/square6 TIER1 imports the composition type, and makes changes like adding further port 
prototypes, component prototypes and connector prototypes (red color in B). TIER1 
considers these changes as “private” and does not return these changes to the OEM. 
/square6 OEM changes the composition, e.g. by adding some port prototypes and removing 
others (C). OEM exports the composition type and passes it to the TIER1 
/square6 TIER1 imports the composition type, and expects that the changes of the OEM are

### Page 6

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
incorporated as well as the changes done by the TIER1 (D) 
 
Composition1 
SWC2 
Composition1 
SWC1 
SWC2 
Composition1 
SWC2 
Composition1 
SWC1 
SWC2 
OEM Workspace TIER1 Workspace 
A B
C D 
Figure 2: Import/Update Example 2 
 
4 Approach 
The import process in DaVinci Developer considers individual objects within the import 
context (set of AUTOSAR XML files or DCF files) and the workspace, see Figure 3. The 
objects are identified by the combination of object type and object short name. Based on 
this identification, the set of objects may be completely disjunctive, or (partially) overlap.

### Page 7

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
Workspace 
Obj1 
Obj2 
Obj3 
Import Context 
Import 
Obj2 
Obj3 
Obj4 
 
Figure 3: Import Context and Workspace 
 
The import mode of an object controls the behavior of DaVinci Developer during the 
import process. The import mode is expressed from the target workspace point of view 
with the following options 
/square6 Keep 
The object in the workspace is not changed 
/square6 Overwrite 
The object in the workspace is overwritten by the imported object 
 
DaVinci Developer supports the following ways to define the import mode of the objects 
/square6 Interactively during the import process (user decision not persistent) 
/square6 Via difference analysis before starting the import process (user decision not 
persistent) 
/square6 By presetting the import mode (persistent) 
The user can select the approach individually for each import process by checking the 
according options in the import dialog. 
4.1 Definition of import mode via difference analysis 
Before running the import process DaVinci Developer opens a dialog showing the 
differences between the objects in the workspace and in the import context. This

### Page 8

User Manual Data Import 
2011, Vector Informatik GmbH Version: 2.0 
 
difference dialog allows the user to browse the differences and select the import mode 
(“Keep” or “Overwrite”) for each object. 
4.2 Interactive definition of import mode 
During the import process DaVinci Developer raises dialogs allowing the user to define the 
import mode. Such dialog is raised for each individual object. For convenience reasons, 
these dialogs offer the option to remember the selected import mode for all other objects of 
the same type, or for all remaining objects. 
The interactive definition of import mode offers “Merge object” as import mode. This option 
is relevant for objects, which have sub-objects. It performs an additive merge of the sub-
objects. Instead of the import mode “Keep”, the option “Create new object” is offered. This 
option leaves the existing objects in the workspace unchanged, and creates a new object 
(with different name) instead. 
4.3 Preset of import mode (automatic merge) 
For the following types of objects: 
/square6 Port prototypes 
/square6 Component prototypes 
the import mode (“Keep” or “Overwrite”) can be preset. So this approach is especially 
useful in case the import process will be repeated in future. These settings become 
effective, if the user chooses “Overwrite” as import mode for a component type. 
4.3.1 Preparation of workspace 
Before running the import process the user can specify the import mode as attribute for 
each object. These attributes are persistently stored in the workspace. To enable

*Excerpt: first 8 of 12 pages shown.*
