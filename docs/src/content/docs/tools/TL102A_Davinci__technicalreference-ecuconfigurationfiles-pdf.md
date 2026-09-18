---
title: 'TL102A_Davinci — TechnicalReference_EcuConfigurationFiles'
description: 'Converted PDF document TechnicalReference_EcuConfigurationFiles.pdf from module TL102A_Davinci.'
sidebar:
  hidden: true
---

> **Source:** `TechnicalReference_EcuConfigurationFiles.pdf` (PDF, 223 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 34; title: Microsoft Word - TechnicalReference_EcuConfigurationFiles.doc; author: viscs

## Converted content

### Page 1

ECU-C File Handling 
Technical Reference 
 
 
 
 
Version 1.13 
 
 
 
 
 
 
Authors: Michael Schuele, Matthias Wernicke 
Version: 1.13 
Status: released (in preparation/completed/inspected/released)

### Page 2

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
2 / 34 
History 
 
Author Date Version Remarks 
M. Schuele 2009-02-19 0.1.0 Initial version 
M. Schuele 2009-04-11 1.0.0 final version 
M. Wernicke 2009-04-17 1.1 Review and update 
M. Schuele 2009-08-03 1.2 Added description of difference dialog 
M. Schuele 2010-01-27 1.3 Added new ECU-C parameters for DaVinci 3.0 
M. Wernicke 2010-01-28 1.4 Review and update 
M. Schuele 2010-05-05 1.5 Introduced different but equivalent parameter values 
M. Schuele 2010-05-14 1.6 Added new ECU-C parameters for DaVinci 3.0 SP2 
M. Schuele 2010-07-20 1.7 Added new ECU-C parameters for DaVinci 3.0 SP3 
M. Schuele 2010-11-29 1.8 Added new ECU-C parameters for DaVinci 3.0 SP4 
M. Schuele 2011-05-06 1.9 ComTimeoutFactor synchronization is configurable 
M. Schuele 2012-02-02 1.10 Added new ECU-C parameters for DaVinci 3.0 SP5 and 3.1 
M. Schuele 2012-08-30 1.11 Added a note about AUTOSAR 4 
M. Schuele 2013-05-03 1.12 Added new ECU-C parameters for DaVinci 3.5 
M. Schuele 2014-03-27 1.13 Added SchM config to Rte section

### Page 3

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
3 / 34 
Contents 
1 Overview ............................................................................................. ............................ 5 
1.1 Intended Audience .................................................................................... ...... 5 
1.2 Terms and Acronyms ................................................................................... .... 5 
2 The ECU-Configuration Process ........................................................................ ........... 7 
2.1 The ECU-Configuration File ........................................................................... . 8 
3 DaVinci DEV and the ECU-C file ....................................................................... ........... 11 
3.1 Project Assistant..................................................................................... ........ 11 
3.2 Initial synchronization (bi-directional update) .................................................. 11 
3.3 Automatic synchronization ............................................................................ 12 
3.4 ECU-C file locking ................................................................................... ...... 12 
3.5 BSWMD files .......................................................................................... ....... 13 
3.5.1 Pre- and Recommended config sections ....................................................... 13 
3.6 Synchronizing an ECU-C file ......................................................................... 13 
3.6.1 Step 1: Analysis of the RTE configuration in the workspace .......................... 14 
3.6.2 Step 2: Comparison of workspace and ECU-C file ..................................

### Page 4

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
4 / 34 
4.6.2 Equivalent parameter values ......................................................................... 27 
4.7 Board ................................................................................................ ............ 27 
4.7.1 Parameters ........................................................................................... ........ 27 
4.7.2 Equivalent parameter values ......................................................................... 28 
4.8 ComSignals and ComSignalGroups .............................................................. 28 
4.8.1 dbc files ............................................................................................ ............. 28 
4.8.2 ECU-Extract .......................................................................................... ........ 28 
4.8.3 AUTOSAR 2.1 .......................................................................................... ..... 29 
4.8.4 AUTOSAR 3.x .......................................................................................... ..... 29 
4.8.5 Relevant ComSignals .................................................................................. .. 29 
4.8.6 Callbacks ............................................................................................ .......... 29 
5 Best practices ....................................................................................... ....................... 31 
5.1 Always work on the latest communication databases .................................... 31 
5.2 Do not edit the same module configuration in different tools at the same 
time .............................................................................................

### Page 5

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
5 / 34 
1 Overview 
DaVinci Developer is part of Vector’s solution for AUTOSAR compatible ECU 
development. It is used to configure and generate the Rte in AUTOSAR 3.x based projects 
and therefore interacts with other BSW configurators through the ECU-Configuration file. 
This document describes the configuration process r elated to DaVinci Developer from a 
technical point of view, trying to give the user a better understanding of the internal 
processes and how the tool reacts in different situations. 
 
 
 
Note 
Starting with DaVinci Developer 3.3, AUTOSAR 4.0 ba sed software designs can be 
created and edited. However, the configuration and generation of the AUTOSAR 4.0 
Rte has been moved from DaVinci Developer to DaVinc i Configurator Pro. Therefore 
this document is only relevant for AUTOSAR 3.x based projects. 
 
1.1 Intended Audience 
This document aims at ECU developers who are involv ed in the AUTOSAR compatible 
ECU-Configuration process and use DaVinci Developer to configure and generate the Rte 
module. 
As DaVinci DEV updates the ECU-Configuration file a utomatically during save and load of 
a workspace, the presented information is not essen tial when working with the tools but 
provides some additional information how the ECU-Co nfiguration process is handled 
behind the scenes. 
1.2 Terms and Acronyms 
Term Definition 
DaVinci DEV DaVinci Developer 
NWD Network Designer 
AR AUTOSAR – Automotive Open System Architecture 
GUI Graphical user interface 
Rte Runtime environment 
BSW Basic Software 
BSWMD Basic Software Module Description

### Page 6

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
6 / 34 
ECU-C file ECU-Configuration file 
ECU-C-Synchronization Synchronization of DaVinci DE V workspace with the 
data in an ECU-C file

### Page 7

ECU-C File Handling Technical Reference 
 2014, Vector Informatik GmbH Version: 1.13 
 
7 / 34 
2 The ECU-Configuration Process 
 
Vector 
DaVinci DEV 
ECU Extract of 
System Description 
SW-Components 
Communication 
Vector 
DaVinci 
Configurator Pro 
RTE 
ECU Cfg 
Descr 
BSW 
Basic Software 
Module Description 
 
Figure 2-1 Basic SW Configuration process 
Figure 2-1 displays the ECU configuration process a s it is supported by Vector’s 
AUTOSAR solution. All configuration tools read from and write to a common ECU-
Configuration file which will be used by the differ ent BSW code generators after the 
configuration of all modules has been completed. 
The various BSW modules are part of different layer s of the AUTOSAR stack with the Rte 
lying on top. Whenever one module utilizes another one its configuration likely depends on 
the configuration of the utilized module and the co nfigurator has to read or even write not 
only the configuration section corresponding to his own module but also the section of the 
other module. 
Since this document is focused on DaVinci DEV, chapter 4 describes th

*Excerpt: first 8 of 34 pages shown.*
