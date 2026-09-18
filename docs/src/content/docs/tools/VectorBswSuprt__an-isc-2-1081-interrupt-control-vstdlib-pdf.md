---
title: 'VectorBswSuprt — AN-ISC-2-1081_Interrupt_Control_VStdLib'
description: 'Converted PDF document AN-ISC-2-1081_Interrupt_Control_VStdLib.pdf from module VectorBswSuprt.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-2-1081_Interrupt_Control_VStdLib.pdf` (PDF, 189 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 13; title: Application Interrupt Control with VStdLib; author: Patrick Markl

## Converted content

### Page 1

Application Interrupt Control with VStdLib 
Version 1.0 
2008-08-06 
Application Note AN-ISC-2-1081 
 
 
 
Author(s) Patrick Markl 
Restrictions Restricted Membership 
Abstract This application note explains how the application can control interrupt handling via the 
VStdLib and which constraints apply. 
 
 
Table of Contents 
 
 1 
Copyright © 2008 - Vector Informatik GmbH 
Contact Information: www.vector-informatik.com or ++49-711-80 670-0 
1.0 Overview ..........................................................................................................................................................1 
1.1 Introduction....................................................................................................................................................1 
2.0 Interrupt Control by Application .......................................................................................................................3 
2.1 Constraints ....................................................................................................................................................3 
2.1.1 Constraint 1: Nested Calls ..........................................................................................................................3 
2.1.2 Constraint 2: Recursive Calls when Disabling CAN Interrupts...................................................................3 
2.1.3 Constraint 3: No Locking when Disabling CAN Interrupts..........................................................................3 
3.0 Solution ............................................................................................................................................................6 
3.1.1 Nested Calls......................................................................

### Page 2

Application Interrupt Control with VStdLib 
 
 
 
 2 
Application Note AN-ISC-2-1081 
 
 
The second option (OSEK) is to configure the VStdLib in a way that locking of interrupts is done by means of 
OSEK OS functions. The third and last option (User defined) requires the application to perform the 
locking/unlocking functionality within callback functions. 
This application note focusses mainly on the third option. It describes the way the application has to implement the 
callback functions required by the VStdLib. 
 
 
Figure 2: Configuration of interrupt control by application 
 
Figure 2 shows the VStdLib configuration dialog, if interrupt control by application is configured. The user has to 
enter the names of two functions in the dialog, which will be called by the VStdLib in order to lock/unlock interrupts. 
If the user has specified the callback function names as shown in figure 2, the application must provide the 
implementations of these two two functions. The prototypes are: 
 
void ApplNestedDisable(void); 
void ApplNestedRestore(void); 
 
From now on these two function names will be used within this application note. 
These two functions are called by the VStdLib, in case any Vector component requests a lock for a critical section. 
The user has to make sure that the locking mechanism within these two functions is sufficient to protect data. This 
depends heavily on the architecture of the application. The more priority levels exists, which call Vector functions, 
the more restrictive the lock must be. 
 
 
Please check the technical references of the other Vector components for restrictions regarding the call 
context of the API functions.

### Page 3

Application Interrupt Control with VStdLib 
 
 
 
 3 
Application Note AN-ISC-2-1081 
 
2.0 Interrupt Control by Application 
This configuration option is usually used, if a global lock is not desired by the user or special lock mechanisms are 
used. Once this option is configured, there are two functions to be provided by the application. The user can 
specify the names of these functions in the configuration dialog of the VStdLib. The VStdLib calls these functions 
instead of directly locking/unlocking interrupts. This means, if any Vector component requests an interrupt lock, it is 
finally performed by the application provided functions. 
The first function is called, in order to perform a lock operation. It is expected, that the application function stores 
the current interrupt state(or any other), in order to restore it later. The second function is to restore the previously 
saved lock state. 
The implementation of these two functions is up to the user. The user may lock just certain interrupt sources or set 
a mutex, semaphore or whatever ensures consistent data and fulfills the call context requirements, described in the 
Vector component specific technical references. 
2.1 Constraints 
The usage of Interrupt Control by Application has some constraints, which have to be taken into account. The 
following chapters describe them. 
2.1.1 Constraint 1: Nested Calls 
It is expected that the two callback functions (ApplNestedDisable()/-Restore()) are implemented in a way that 
nested calls are possible. This means if the function ApplNestedDisable() was called by some software component 
it may happen that this function is called again from somewhere else. This has to be taken into account when 
saving and restoring the interrupt state! The implementer of these two 

### Page 4

Application Interrupt Control with VStdLib 
 
 
 
 4 
Application Note AN-ISC-2-1081 
 
 
/* CAN Interrupt will be never locked in this example!!! */ 
void CanCanInterruptDisable(CAN_CHANNEL_CANTYPE_ONLY) 
{ 
 ApplNestedDisable(); 
 Lock CAN interrupts 
 ApplNestedRestore(); 
} 
 
void ApplNestedDisable(void) 
{ 
 Save current CAN interrupt state(); 
 Lock CAN Interrupts(); 
} 
 
void ApplNestedRestore(void) 
{ 
 Restore CAN interrupts to previous state(); 
} 
 
Figure 3 shows what happens in this case. The function CanCanInterruptDisable() calls ApplNestedDisable() in 
order to protect an internal counter. This lock function disables the CAN interrupts, afterwards the CAN driver’s 
function locks the CAN interrupts too. The next thing is to call ApplNestedRestore() which again is implemented by 
the application and restores the previous CAN interrupt state – in this case enables the CAN interrupts. Now an 
inconsistency exists. The code which called CanCanInterruptDisable() assumes locked CAN interrupts, but they 
aren’t

### Page 5

Application Interrupt Control with VStdLib 
 
 
 
 5 
Application Note AN-ISC-2-1081 
 
sd FailedLock
Component CAN Driver Application CAN Controller
CanCanInterruptDis able
VStdGlobalInterruptDis able
Lock CAN Interrupt
Lock CAN Interrupt
VStdGlobalInterruptRes tore
Unlock CAN Interrupt
 
Figure 3: Sequence diagram of CanCanInterruptDisable()

### Page 6

Application Interrupt Control with VStdLib 
 
 
 
 6 
Application Note AN-ISC-2-1081 
 
3.0 Solution 
This chapter proposes a solution and a code examples, to overcome the constraints 1 and 3 described in the 
previous chapters. 
3.1.1 Nested Calls 
Solving the first issue – nested calls – is simply done by introducation of a nesting counter. The callbacks 
implemented by the application need to manage this counter. The counter is to be incremented, if the function to 
lock interrupts is called and decremented if the unlock function is called. The application has to take care to 
initialize this counter, before any Vector function is called, in order to ensure a consistent interrupt locking. 
The interrupt state is to be modified only if the counter has the value zero. If the value is greater than zero, the 
counter is just maintained. The following code example shows, how this nested counter could be implemented. 
 
/* Global variable as nesting counter */ 
vuint8 gApplNestingCounter; 
 
/* Must be called before the Vector components are initialized! */ 
void SomeApplicationInitFunction(void) 
{ 
 gApplNestingCounter = (vuint8)0; 
} 
 
void ApplNestedDisable(void) 
{ 
 /* check counter – lock if counter is 0 */ 
 if((vuint8)0 == gAp

*Excerpt: first 8 of 13 pages shown.*
