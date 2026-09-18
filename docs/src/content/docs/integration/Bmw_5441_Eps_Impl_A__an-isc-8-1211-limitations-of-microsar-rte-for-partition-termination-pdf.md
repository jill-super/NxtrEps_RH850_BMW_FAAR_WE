---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1211_Limitations_of_MICROSAR_RTE_for_Partition_Termination'
description: 'Converted PDF document AN-ISC-8-1211_Limitations_of_MICROSAR_RTE_for_Partition_Termination.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1211_Limitations_of_MICROSAR_RTE_for_Partition_Termination.pdf` (PDF, 214 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 3; title: Limitations of MICROSAR RTE for Partition Termination; author: Jonas Wolf

## Converted content

### Page 1

Limitations of MICROSAR RTE for Partition Termination 
Version 1.0 .0 
2017 -08-15 
Application Note AN-ISC -8-1211 
Author Jonas Wolf 
Restrictions Customer Confidential – Vector decides 
Abstract This application note describes the scenarios it is considered possible to terminate an 
OS application, in which the MICROSAR RTE is used, using the MICROSAR OS. 
 
 
Table of Contents 
1 Overview ........................................................................................................................................ 2 
2 Limitations of MICROSAR RTE .................................................................................................... 2 
3 Additional Resources ................................................................................................................... 3 
4 Contacts ......................................................................................................................................... 3

### Page 2

Limitations of MICROSAR RTE for Partition Termination 
Copyright © 2017 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Overview 
Terminating and restarting of partitions (i.e. OS applications) is an AUTOSAR feature supported by 
Vector’s Operating System (OS). Vector’s MICROSAR Runtime Environment (RTE), however, does 
not implement termination or restart of partitions. 
2 Limitations of MICROSAR RTE 
Terminating or restarting OS applications is problematic, for example when the following 
dependencies between different OS applications exist: 
> Trusted function calls, 
> Client/server communication, 
> Queued sender/receiver communication, 
> Mode management, 
> Dependencies on states on application level 
These kinds of dependencies rely on either OS objects, like events, or RTE states, e.g. queue state. If 
one OS application is restarted, the other OS application(s) may have an inconsistent view on these 
objects or states. There may be also dependencies on the application level that are not obvious to 
identify, e.g. due to functional dependencies. 
For implementing termination or restarting of OS applications it must be considered that termination or 
restart may happen exactly at a point in time when one of the activities above is being executed, e.g. 
during a client/server call. 
The restarted OS applications need to establish their initialization state again. This requires initializing 
all variables, e.g. states and inter-runnable variables to their initial values. Due to a different system 
state in other partitions, this will most likely break functionality if no measures on the application level 
are taken. 
 
The MICROSAR RTE currently does not implement functionality for terminating or restarting of OS 
application

### Page 3

Limitations of MICROSAR RTE for Partition Termination 
Copyright © 2017 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
3 Additional Resources 
VECTOR TECHNICAL REFERENCES 
Technical Reference RTE 
Technical Reference OS 
4 Contacts 
For a full list with all Vector locations and addresses worldwide, please visit http://vector.com/contact/.
