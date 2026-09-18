---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1196_Distributing_BSW_Components_across_Partitions'
description: 'Converted PDF document AN-ISC-8-1196_Distributing_BSW_Components_across_Partitions.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1196_Distributing_BSW_Components_across_Partitions.pdf` (PDF, 400 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 7; title: Distributing BSW Components across Partitions; author: Wolf, Jonas

## Converted content

### Page 1

Distributing BSW Components across Partitions 
Version 1.2 
2017 -05-17 
Application Note AN-ISC -8-1196 
Author Wolf, Jonas 
Restrictions Customer Confidential – Vector decides 
Abstract MICROSAR BSW is supposed to be executed in one memory partition (with some 
exceptions). Architectural constraints, e.g. a safety concept, may require distributing 
MICROSAR BSW across different memory partitions. This application note describes 
the general approach and common techniques for distribution. 
 
 
Table of Contents 
1 Overview ........................................................................................................................................ 2 
2 Introduction of Partitioning .......................................................................................................... 2 
3 Techniques for Crossing Partitions ............................................................................................ 3 
3.1 Trusted Functions ................................................................................................................ 3 
3.2 Non-trusted Functions .......................................................................................................... 3 
3.3 Inter OS Application Communicator (IOC) ........................................................................... 3 
3.4 Sharing Data ........................................................................................................................ 3 
4 Hooking into Interfaces ................................................................................................................ 4 
4.1 Example Code...................................................................................................................... 6 
4.1.1 Source File of A (A\A.c) ......

### Page 2

Distributing BSW Components across Partitions 
Copyright © 2017 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Overview 
AUTOSAR was initially developed for single core microcontrollers without memory protection unit 
(MPU). The availability of more powerful microcontrollers and the introduction of ISO 26262 led to new 
concepts in AUTOSAR addressing these changes. 
This document provides an approach how to distribute basic software across partitions on one core. 
Distributing the basic software across different cores is out of scope of this application note. The term 
basic software is used in this application note for all software components below the Runtime 
Environment (RTE), i.e. AUTOSAR modules, like ECUM or COM as well as complex drivers (CDs). 
Above the RTE, i.e. for application software components (SWC), partitioning is usually automatically 
handled by configuration of the RTE. Thus, this is also out of scope for this application note. 
 
Figure 1-1 Basic Software 
Apart from a few exceptions it is not possible to distribute the basic software into different partitions by 
configuration. This application note describes an approach for partitioning the basic software. It details 
the available techniques for implementing the partition crossing and shows an example use-case. 
An AUTOSAR operating system with Scalability Class 3 (SC3) and an MPU is required for memory 
partitioning. The term partition and OS Application are used synonymously. 
2 Introduction of Partitioning 
Use the following three step approach to introduce working and effective partitioning of the basic 
software: 
1. Define partitioning scheme 
Use the software architecture of the ECU to describe the partitions and assign all SWCs and basic 
software c

### Page 3

Distributing BSW Components across Partitions 
Copyright © 2017 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Note 
A lot of interfaces between BSW modules can be deactivated by configuration. Evaluate 
whether deactivation of the interface is an option and deactivate the interface if possible. 
This may especially apply for interfaces to DEM and DET. If the interface is deactivated, 
there is no need to introduce cross-partition calls. 
 
 
3 Techniques for Crossing Partitions 
3.1 Trusted Functions 
Trusted Functions are services exported by trusted applications for the use by other applications and 
are realized by the operating system (OS). Calling Trusted Functions usually implies switching from 
user mode to supervisor mode (and back when returning). 
Trusted Functions are executed on the stack of the caller. 
AUTOSAR specifies that interrupts have to be enabled when calling a Trusted Function. To ensure 
data consistency for an exclusive area in which the Trusted Function is called, OS resources can be 
used instead of disabling interrupts. This restriction does not apply to versions of Generation7 of 
MICROSAR OS. They do not require enabled interrupts when calling Trusted Functions. 
For more information on Trusted Functions see AUTOSAR SWS OS (Version 4.3, Section 8.4.4) and 
Technical Reference MICROSAR OS (e.g. Version 1.8.0, Section 3.3). 
3.2 Non-trusted Functions 
Non-trusted Functions are services exported by non-trusted OS applications for the use by other 
applications and are realized by the operating system (OS). They have the following characteristic: 
> They run in user mode. 
> They run with the MPU access rights of the owning OS application. 
> They perform a stack switch to specific and secured Non-truste

### Page 4

Distributing BSW Components across Partitions 
Copyright © 2017 - Vector Informatik GmbH 4 
Contact Information: www.vector.com or +49-711-80 670-0 
detect if data was read by the receiver. The two flags are readable from sender and receiver, but 
writable only by their respective owner. 
4 Hooking into Interfaces 
Usually Trusted Functions and Non-trusted Functions are not used by AUTOSAR basic software 
components. They can, however, be introduced manually by using the technique shown in the 
following example. 
There are two components A and B. A calls a function in B (B_func). Both components are assigned 
to different partitions. A is allocated to a non-trusted partition. B is allocated to a trusted partition. 
Thus, the function call from A to B needs to be redefined to a Trusted Function call. 
The original call and include graph are shown in Figure 4-1 and Figure 4-2. 
 
Figure 4-1 Original call graph 
 
Figure 4-2 Original include graph 
Redefinition of functions requires the introduction of a new component Bmod. Bmod will redefine the 
B_func to a different function name with the same signature, i.e. the Trusted Function configured in 
the operating system. In this example the Trusted Function call is named B_mod_B_func. The 
Trusted Function call in the operating system switches the memory protection to settings defined for 
the trusted application and finally calls B_func. 
Figure 4-3 shows the modified call graph. 
 
Figure 4-3 Modified call graph 
To make A call a function in Bmod instead of B, the include graph needs to modified as well. Figure 
4-4 shows the modified include graph.

### Page 5

Distributing BSW Components across Partitions 
Copyright © 2017 - Vector Informatik GmbH 5 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Figure 4-4 Modified include graph 
To make this modification to the include graph the include path that pointed to B is modified to point to 
Bmod. Please note that in Bmod\B.h the include path is resolved in the header file itself and not using 
include path compiler options (see line 8 of Bmod\B.h below). 
The approach described above can also be used if no preprocessor define in the source file exists. 
The build system can also be used to set those defines individually for each source file, e.g. using the 
–D compiler option available for several compilers. All Vector components provide such a define in 
source code (see line 3 of B.c below).

### Page 6

Distributing BSW Components across Partitions 
Copyright © 2017 - Vector Informatik GmbH
