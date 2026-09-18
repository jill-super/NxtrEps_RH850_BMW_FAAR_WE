---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1207_Synchronization_Cry_Fls'
description: 'Converted PDF document AN-ISC-8-1207_Synchronization_Cry_Fls.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1207_Synchronization_Cry_Fls.pdf` (PDF, 426 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 8; title: Synchronization between AUTOSAR Cry and Fls; author: Bernhard Wissinger

## Converted content

### Page 1

Synchronization between AUTOSAR Cry and Fls 
Version 1.00.03 
2017 -08-14 
Application Note AN-ISC -8-1207 
Author Bernhard Wissinger 
Restrictions Customer Confidential – Vector decides 
Abstract AUTOSAR Crypto and Flash Driver might access a common hardware resource. This 
application note describes possible synchronization mechanisms. 
 
 
Table of Contents 
1 Introduction ................................................................................................................................... 2 
1.1 Access Conflict Types .......................................................................................................... 2 
1.2 Dependency of Access Conflics to the ECU use case ........................................................ 3 
2 Use Case Description ................................................................................................................... 3 
3 Synchronization Methods of SecOC and Fls ............................................................................. 4 
3.1 Prevent Execution of SecOC_MainFunction ....................................................................... 4 
3.2 Prevent Execution of Cry Function ...................................................................................... 5 
3.3 Optimized Execution Prevention .......................................................................................... 5 
3.4 Interrupt Fls Operation ......................................................................................................... 6 
3.5 Asynchronous Operation of SecOC ..................................................................................... 7 
4 Synchronization Method for Key Management .......................................................................... 8 
5 Contacts

### Page 2

Synchronization between AUTOSAR Cry and Fls 
Copyright © 2017 - Vector Informatik GmbH 2 
Contact Information: www.vector.com or +49-711-80 670-0 
1 Introduction 
AUTOSAR defines Crypto Driver (Cry) and Flash Driver (Fls) as MCAL modules for independent 
hardware modules. But as the crypto module also provides key storage functionality, this is often 
implemented in the microcontroller by using a shared flash unit. This can lead to race conditions , if 
AUTOSAR Crypto Driver and Flash Driver are used concurrently. 
 
Figure 1 - Race Condition during Flash Memory Access 
This application note describes several synchronization methods and gives advice which method 
should be applied. The synchronization itself must be implemented by the application during the 
integration of the MICROSAR stack, as the used method depends on the system layout and 
requirements. 
 
 
Caution 
The occurrence and effect of the race condition heavily depends on the used 
microcontroller. Please double-check whether your specific hardware is affected and 
confirm whether the methods described in this application note are applicable to your 
system. 
 
 
 
Caution 
The examples in this application note are not thoroughly tested. The user must verify the 
functionality for the intended use case. Vector´s liability shall be expressly excluded to the 
extent admissible by law or statute. 
 
1.1 Access Conflict Types 
Table 1 lists possible access conflict types. In this application note, it is assumed that each of these 
combinations will lead to a race condition and must be prevented. E.g. even if the Crypto driver 
performs only a read access to the key (like MacVerify), a parallel read access of the flash driver to 
the hardware is not allowed. 
If the used microcontroller is less restrictive, a

### Page 3

Synchronization between AUTOSAR Cry and Fls 
Copyright © 2017 - Vector Informatik GmbH 3 
Contact Information: www.vector.com or +49-711-80 670-0 
Crypto Driver Flash Driver Conflict 
Use Key (e.g. MacVerify, MacGenerate) Read Flash Memory Read / Read 
Write Key (e.g. KeyElementSet) Read Flash Memory Write / Read 
Use Key (e.g. MacVerify, MacGenerate) Write Flash Memory Read / Write 
Write Key (e.g. KeyElementSet) Write Flash Memory Write / Write 
Table 1 - Access Conflict Types 
1.2 Dependency of Access Conflics to the ECU use case 
The possibility of an access conflict heavily depends on the ECU use case. As an access conflict can 
only happen if the Flash module and Crypto module are used at the same time, a detailed analysis of 
this use case is needed. 
> E.g. if the Crypto module is used only during ECU run state for secure communication, whereas 
Flash module access is limited to ECU startup and shutdown, no access conflict might occur. 
> The access conflict might be limited to system startup, in case the Crypto module can cache the 
keys in secure RAM and therefore has no need to access data flash during later usage. 
The potential access conflicts need to be analyzed by the user. This application note gives an 
example how to solve such a conflict for secure communication and data flash a ccess. 
 
 
Caution 
The occurrence and effect of access conflicts heavily depend on the ECU use case. 
Please analyze the specific Crypto and Flash use cases in your ECU to confirm potential 
conflicts and to judge for the appropriate resolution method. 
 
2 Use Case Description 
The synchronization methods are discussed based on three different users of Crypto and Flash Driver. 
Please adapt the described concepts in case of a different use case shall be implemented. 
 
 
C

### Page 4

Synchronization between AUTOSAR Cry and Fls 
Copyright © 2017 - Vector Informatik GmbH 4 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Figure 2 - Conflict between Fls and Cry 
3 Synchronization Methods of SecOC and Fls 
This chapter describes synchronization methods between Fls and Cry for the SecOC use case. 
 
 
Caution 
It is assumed that Fls_MainFunction cannot interrupt 
SecOC_MainFunction. E.g. Fls_MainFunction is mapped to the same or a 
lower priority OS task as SecOC_MainFunction. 
 
Table 3 gives an overview and comparison of the different methods which are described in this 
chapter. 
Method Characteristics AUTOSAR Extensions 
3.1 
SecOC messages will not be sent during Fls 
operation. Especially Fls erase might take a long 
time. 
None 
3.2 Same as 3.1 Cry extension “Read Start” interface 
3.3 Less impact on SecOC messages for “short” Fls 
operations 
Fls extension “GetHWStatus” 
3.4 Difficult if Suspend/Resume needs a long time Fls extension “Suspend/Resume” 
3.5 Most complex approach Fls extensions “Suspend/Resume” 
and “asynchronous notification” 
Table 3 – Comparison Matrix 
3.1 Prevent Execution of SecOC_MainFunction 
The current state of Fls can be polled by the function Fls_GetStatus. Therefore 
SecOC_MainFunction should not be called in case Fls_GetStatus returns “busy”. 
 
Fls
Cry
SecOC_MainFunction
Fls_MainFunction
SecOC_MainFunction
Fls_MainFunction
SecOC_MainFunction
cycle time
Fls HW busy
Cry HW busyconflict
no Fls HW 
access in 
this call 
cycle
asynchronous handling of Fls HW

### Page 5

Synchronization between AUTOSAR Cry and Fls 
Copyright © 2017 - Vector Informatik GmbH 5 
Contact Information: www.vector.com or +49-711-80 670-0 
 
Caution 
It is assumed that Fls_GetStatus can be called reentrant. Please confirm this behavior 
for the used Fls module. 
 
 
Figure 3 - Prevent Execution of SecOC_MainFunction 
3.2 Prevent Execution of Cry Function 
This approach is similar to chapter 3.1. But instead of preventing the execution of 
SecOC_MainFunction, an API like Cry_XXX_DataFlashReadStart_Callout would be used. 
With the API Cry_XXX_DataFlashReadStart_Callout, the read permission is checked by the 
Cry driver: this shall be denied in case the Fls is busy. 
The SecOC_MainFunction will retry with the next cyclic call, if the parameter 
SecOCAuthenticationBuildAttempts in SecOC is set accordingly. 
 
 
Note 
The API Cry_XXX_DataFlashReadStart_Callout is not defined by AUTOSAR and 
might not be available for your hardware. 
 
 
3.3 Optimized Execution Prevention
