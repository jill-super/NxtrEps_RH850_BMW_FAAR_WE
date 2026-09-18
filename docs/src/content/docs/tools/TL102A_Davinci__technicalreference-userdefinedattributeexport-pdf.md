---
title: 'TL102A_Davinci — TechnicalReference_UserDefinedAttributeExport'
description: 'Converted PDF document TechnicalReference_UserDefinedAttributeExport.pdf from module TL102A_Davinci.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_UserDefinedAttributeExport.pdf` (PDF, 93 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 11; title: Microsoft Word - TechnicalReference_UserDefinedAttributeExport.doc; author: viscs

## Converted content

### Page 1

User-defined attribute XML-export 
Technical Reference 
 
 
 
 
Version 1.3 
 
 
 
 
 
 
Authors: Michael Hoffmann, Andreas Claus 
Version: 1.3 
Status: released (in preparation/completed/inspected/released)

### Page 2

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
History 
 
Author Date Version Remarks 
Hn 2007-02-02 1.0 Document released 
Cs 2007-11-28 1.1 New document template; minor corrections 
Hn 2008-02-08 1.2 Document updated 
Cs 2012-04-11 1.3 DCF workspaces added; minor corrections 
 
Contents 
1 Overview ......................................... ................................................... ....................... 3
1.1 Terms and Acronyms ............................. ................................................... .. 3
2 User-defined attributes in DaVinci ............... ................................................... ........ 4
2.1 Creating user-defined attribute definition ..... ............................................... 4
2.2 User-defined attribute usage ................... ................................................... . 5
2.3 Creating the XML-export ........................ ................................................... .. 6
3 Design object reference .......................... ................................................... .............. 7
4 Attribute definition resolution .................. ................................................... ............ 8
4.1 Reference of global attribute definition values ............................................. 8
4.2 Reference of local attribute value ............. ................................................... 9
5 DCF Workspaces ................................... ................................................... .............. 10 
5.1 Global attribute definition file ............... ................................................... ... 10 
5.2 Loading attribute definitions .................. ....................................

### Page 3

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
1 Overview 
With the DaVinci Developer 2.1 and later user-defin ed attribute definitions can be 
exported. This document describes the usage of the exported XML file format. 
1.1 Terms and Acronyms 
Term Definition 
DaVinci DEV DaVinci Developer 
AR AUTOSAR – Automotive Open System Architecture 
GUI Graphical user interface 
DCF DaVinci configuration file workspace

### Page 4

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
2 User-defined attributes in DaVinci 
DaVinci DEV are allows the definition of user-defined attributes for certain design elements 
visible within the GUI. 
The set of design elements which are providing the definition of user-defined attributes 
depends on the tool version. 
2.1 Creating user-defined attribute definition 
To create a user-defined attribute definition open the workspace global attribute definition 
table available on the main menu ‘View /barb2right Attribute Definition…’. 
Each user-defined attribute is related to a DaVinci object type and must have a name 
which is unique in the scope of the attribute definition table. 
The definition of minimum, maximum, and default val ue depends on the selected value 
type 
 
Figure 1: Definition of user-defined attribute

### Page 5

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
2.2 User-defined attribute usage 
Attribute definitions can be used at certain design objects of the workspace. For each 
attribute which is defined within the global attrib ute table and associated with the object 
type of the design object, a local value definition can be specified. 
These values are specific for each design object an d are available in the properties dialog 
of the design object. 
A design object can only use those user-defined att ributes which are defined within the 
global attribute definition table. 
 
Figure 2: Definition of a local value of a user-defined attribute

### Page 6

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
2.3 Creating the XML-export 
The export of user-defined attributes is always rel ated to a preceded export of design 
elements. The export can be used with all supported AR versions. 
To create the XML export, select the appropriate de sign element within DaVinci DEV and 
choose the ‘XML Export…’ command from the context menu. 
The export dialog provides an option ‘Export user-d efined attributes’. If this option is 
selected an additional XML output file will be crea ted. The name of the XML file is 
automatically created by using the name of the AR-X ML output file plus the extension 
‘_gen_attr’ (e.g. ‘System_gen_attr.xml’). 
 
 
Figure 3: User-defined attribute export option for XML-exports

### Page 7

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
3 Design object reference 
The design object reference clarifies in which way a certain design object is related to the 
user-defined attribute definition within the attribute export file. 
An AR design object is referenced by an AR referenc e which contains the package path to 
the SHORT_NAME attribute of the referenced AR object. 
This reference is stored within the Reference attribute of the ARObjectReference tag 
within the user-defined attribute export XML file. 
Beside the AR reference the ARObjectReference tag also includes the XML tag of the 
referenced AR element within its Type attribute. 
E.g. for a software component type ‘AP_MySWC’ follo wing reference information is 
exported: 
User-defined attribute export file: 
 
 <ObjectAttributeReference ObjectType =" ComponentType "> 
 <ARObjectReference 
Type =" APPLICATION-SOFTWARE-COMPONENT-TYPE " 
Reference =" /ComponentType/AP_MySWC "> 
</ ARObjectReference > 
…. 
 </ ObjectAttributeReference > 
 
AR-export file: 
 
<AUTOSAR > 
 <TOP-LEVEL-PACKAGES > 
 <AR-PACKAGE > 
 <SHORT-NAME >ComponentType </ SHORT-NAME > 
 <ELEMENTS > 
 <APPLICATION-SOFTWARE-COMPONENT-TYPE > 
 <SHORT-NAME >AP_MySWC </ SHORT-NAME > 
…. 
 </ APPLICATION-SOFTWARE-COMPONENT-TYPE > 
 </ ELEMENTS > 
 </ AR-PACKAGE > 
 </ TOP-LEVEL-PACKAGES > 
</ AUTOSAR >

### Page 8

User-defined attribute XML-export Technical Reference 
 2012, Vector Informatik GmbH Version: 1.3 
 
4 Attribute definition resolution 
The attribute definition resolution shows how a glo bal user-defined attribute definition is 
referenced by a certain design object. 
4.1 Reference of global attribute definition values 
If a design object doesn’t define a local value that is different from the global default value 
definition the user-defined attribute export will o nly export the reference to the relevant 
attribute definition table. This reference ( AttributeDefinitionTableRef ) contains a 
Version and an ID attribute which uniquely identifies the relevant attribute definition table 
of the item (see ‘ AttributeDefinitionTableRef’ of the example below). 
By using the ObjectType attribute information of the ObjectAttributeReference tag 
the set of relevant attribute definitions for this item type can be identified (e.g. 
‘ComponentType ’). 
User-defined attribute export file: 
 
<AttributeDefinition > 
 <AttributeDefinitionTable Version="1.0" ID="{932D3FD0-2F6C-49BF-80CB-D1C3756D3868}" > 
 <Attribute Name =" MySWCEnum " ObjectType =" ComponentType "> 
 <ENUM Default =" Enum2 "> 
 <EnumValue Value =" Enum1 "></ EnumValue > 
 <EnumValue Value =" Enum2 "></ EnumValue > 
 <EnumValue Value =" Enum3 "></ EnumValue > 
 </ ENUM > 
 </ Attribute > 
 </ AttributeDefinitionTable > 
 
 <ObjectAttributeReference ObjectType =" ComponentType "> 
 
<ARObjectReference 
 Type =" APPLICATION-SOFTWARE-COMPONENT-TYPE " 
 Reference =" /ComponentType/AP_MySWC "> 
</ ARObjectReference > 
 
<AttributeDefinitionTabl

*Excerpt: first 8 of 11 pages shown.*
