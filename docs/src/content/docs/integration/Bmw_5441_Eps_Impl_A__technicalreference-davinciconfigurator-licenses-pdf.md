---
title: '_Bmw_5441_Eps_Impl_A — TechnicalReference_DaVinciConfigurator_Licenses'
description: 'Converted PDF document TechnicalReference_DaVinciConfigurator_Licenses.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_DaVinciConfigurator_Licenses.pdf` (PDF, 304 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 16; title: DaVinci Configurator License Handling; author: Michael Hoffmann

## Converted content

### Page 1

DaVinci Configurator License Handling 
Technical Reference 
 
 
Version 1.5 
 
 
 
 
 
 
 
 
 
 
 
Authors Michael Hoffmann 
Status Released

### Page 2

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 2 
based on template version 4.11.3 
Document Information 
History 
Author Date Version Remarks 
Michael Hoffmann 2014-01-02 1.0 
Michael Hoffmann 2014-02-14 1.1 Server Configuration in 3.1 
changed 
Michael Hoffmann 2015-02-10 1.2 Server Configuration in 3.1 
changed; VTT option added 
Michael Hoffmann 2015-04-27 1.3 DaVinci_CFG floating server 
option added 
Michael Hoffmann 2015-05-21 1.4 Pool based licenses added 
Michael Hoffmann 2016-02-01 1.5 Template update 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire.

### Page 3

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 3 
based on template version 4.11.3 
Contents 
1 Introduction................................ ................................ ................................ ................... 5 
2 License Information ................................ ................................ ................................ ...... 6 
2.1 SIP Based License ................................ ................................ ............................. 6 
2.2 Software Based License ................................ ................................ .................... 6 
2.3 Hardware Based Licenses ................................ ................................ ................. 6 
2.4 License Display ................................ ................................ ................................ .. 7 
2.5 Display of License Server Configuration and Options ................................ ........ 7 
3 License Server Configuration ................................ ................................ ...................... 8 
3.1 Server Configuration ................................ ................................ .......................... 8 
3.1.1 Settings ................................ ................................ .............................. 9 
3.2 Server Option Usage Configuration ................................ ................................ . 10 
3.3 Settings File Example ................................ ................................ ...................... 10 
4 Pool Licence Handling ................................ ................................ ............................... 12 
4.1 Standard Licenses ................................ ................................ ....

### Page 4

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 4 
based on template version 4.11.3 
Illustrations 
- 
Tables 
Table 2-1 License appearance ................................ ................................ ................... 7 
Table 3-1 Settings file locations ................................ ................................ .................. 8 
Table 3-2 License precedence................................ ................................ .................... 9 
Table 3-3 Server options ................................ ................................ .......................... 10

### Page 5

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 5 
based on template version 4.11.3 
1 Introduction 
The DaVinci Configurator application can be activated by a SIP license and dongle or 
FlexNet based license. Both, the dongle and the FlexNet based license, provide the .PRO 
option + supplemental options. These options activ ate additional product functionality 
within the DaVinci Configurator. 
This document describes in which order the available licenses are applied and used by the 
DaVinci Configurator.

### Page 6

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 6 
based on template version 4.11.3 
2 License Information 
Detailed information about the current available an d used licenses can be obtained by 
starting the DaVinci Configurator application and opening the ‘Licenses’ dialog (Help > 
Licenses). 
This dialog shows the current SIP license details (‘Show SIP License Details’ button) and 
the current tool license details (‘Show Tool License Details’). 
The tool license details dialog provides three sections: 
 SIP-based licenses 
 Software-based licenses 
 Hardware-based licenses (USB-dongle) 
2.1 SIP Based License 
This section shows the current ly available SIP license. A SIP license activates the BASE 
option of the DaVinci Configurator application. 
2.2 Software Based License 
This table lists all avail able FlexNet license information ( server based or local) that can 
potentially be used by the DaVinci Configurator application. 
For server based licenses the floating licensing and the pool licensing model is supported 
(see 3.1 for details). 
The actual used license model is shown in the label of the ‘License server’ property of the 
‘Licenses’ dialog. It can be ‘Pool’ or ‘Floating’, depending on which license model is 
defined within the server configuration file (see chapter 3 for details). 
2.3 Hardware Based Licenses 
This section contains all dongle based licenses detected by the application. 
 
 
Note 
Aladdin dongles (blue dongles) cannot be used in 64-Bit Windows with DaVinci 
Configurator executed in 64-Bit mode (which is the default on 64-Bit Windows). 
In that case the new Keyman dongles need to be used instead.

### Page 7

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 7 
based on template version 4.11.3 
2.4 License Display 
Each entry within the sections of the license details dialog will have one of the following 
colors indicating whether the license is valid or not and used or not. Refer to following 
table for details. 
License Appearance 
Color Description 
black License is valid. 
blue License is valid and used by the current running application instance. 
grey License is expired. 
Table 2-1 License appearance 
2.5 Display of License Server Configuration and Options 
In case a FlexNet license server is configured (see 3.1 for details) the license details 
dialog shows the server configuration details and the according option configuration below 
the software-based licenses grid.

### Page 8

Technical Reference DaVinci Configurator License Handling 
© 2016 Vector Informatik GmbH Version 1.5 8 
based on template version 4.11.3 
3 License Server Configuration 
Flexnet licenses can be provided by using a license server. The DaVinci Configurator 
application only accesses these licenses when: 
 No .PRO option is available at the local PC 
 A valid license server connection is configured 
 The DaVinci_CFG option within the settings.ini file is not explicitly set to ‘0’ (see also 
3.2 and 3.3 for details) 
 The pool license model is used and no .PRO option (provided by a single-seat license 
or dongle) is available at the local PC 
Otherwise the server isn’t accessed. 
3.1 Server Configuration 
The DaVinci Configurator application detects a license server connection if a 
Settings.ini file is either placed in the executable folder or in the common files folder 
for Vector applications. 
The search order is identical to the order of appearance in table Table 3-1. 
Setting File Locations 
Location Environment 
DaVinciCFG.exe directory All 
%COMMONPROGRAMFILES(X86)%\Vector\DaVinci All 
Table 3-1 Settings file locations

*Excerpt: first 8 of 16 pages shown.*
