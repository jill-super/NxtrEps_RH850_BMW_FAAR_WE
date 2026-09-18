---
title: '_Bmw_5441_Eps_Impl_A — IssueReport_CBD1700369'
description: 'Converted PDF document IssueReport_CBD1700369.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `IssueReport_CBD1700369.pdf` (PDF, 785 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 202; title: -; author: -

## Converted content

### Page 1

Issue Report
1
License Number Customer
CBD1700369 Nexteer Automotive Corporation
Package: MSR BAC 4.x - ECU product "Electric Power 
Steering"
Maintenance Expiry Date
2018-08-01
SIP Version
19.06.14
SLP Delivery Number
MSR BAC 4.x D04
Report Creation Date
2018-01-30
Contact
In case of questions or the need for an update of the basic software delivery, please contact 
EmbeddedSupport@us.vector.com or your Vector contact person.
Table of Contents
1. Introduction
1.1 Resolving Issues
1.2 Issue Classification
2. New Issues
2.1 Safety Relevant Issues: 7
2.2 Runtime Issues without Workaround: 16
2.3 Runtime Issues with Workaround: 38
2.4 Not Released Functionality: 9
2.5 Apparent Issues: 93
2.6 Compiler Warnings: 17
3. New Issues for Information: 0
4. Report Legend
5. 3rd Party Software Issues
6. Quality Management Contact

### Page 2

Issue Report
2
1. Introduction
1.1 Resolving Issues
Reported issues are not automatically fixed with the next update delivery.
If a reported issue shall be fixed, please contact Vector agree on the issues that can be fixed with 
upcoming deliveries. 
Please note that Vector may fix issues without explicit request.
1.2 Issue Classification
This Issue Report provides issues that have been detected since the last report. The issues have 
been classified to facilitate the assessment of their impact:
The chapter 'New Issues' lists issues that have been detected since the last report and which could 
not be excluded based on the use-case defined in the questionnaire. The issues are classified as 
follows:
• Safety Related Issues: Safety related issues have impact on the functional safety of the 
software module. If this issue interferes with the functional safety concept of the ECU, this 
module (or module configuration) must not be used for serial production in a safety-related 
project. The effect of the issue to the ECU functionality and functional safety has to be 
analyzed by the user as the software usage and its configuration is not known by Vector. The 
risk of change has also to be taken into account.
• Runtime Issues without Workaround: Runtime issues without a workaround require an 
update of the software delivery in case the issue affects the ECU overall functionality. The 
effect of an issue to the ECU functionality has to be analyzed by the customer as the software 
usage and its configuration is not known by Vector. The risk of change has also to be taken 
into account.
• Runtime Issues with Workaround: It is not recommended to update a delivery due to a 
runtime issue with a documented workaround. The effect of an issue to the ECU functionality 
has to be anal

### Page 3

Issue Report
3
2. New Issues
2.1 Safety Relevant Issues
Safety related issues have impact on the functional safety of the software module. If this issue 
interferes with the functional safety concept of the ECU, this module (or module configuration) 
must not be used for serial production in a safety-related project.
The effect of the issue to the ECU functionality and functional safety has to be analyzed by the 
user as the software usage and its configuration is not known by Vector. The risk of change has 
also to be taken into account.
Index
ESCAN00097518 CRC32 calculations deliver wrong results
MemService_AsrNvM@Implementation
ESCAN00097644 RTE dereferences NULL_PTR after execution of a mapped server runnable
Rte_Core@Implementation
ESCAN00097829 Service 0x22: Overwritten call stack
Diag_Asr4Dcm@Implementation
ESCAN00097901 Rx Deferred Event Cache leads to unexpected ECU behaviour under high load
Il_AsrComCfg5@Implementation
ESCAN00097911 Deferred PDUs are not processed using deferred event Cache
Il_AsrComCfg5@Implementation
ESCAN00097946 Interrupts are still disabled when returning from ResumeOSInterrupts or 
ReleaseSpinlock after the corresponding suspension API has been interrupted
Os_CoreGen7@Implementation
ESCAN00098052 Undefined behavior of OS after context switch (RH850)
Os_PlatformRH850Gen7@Implementation

### Page 4

Issue Report
4
ESCAN00097518 CRC32 calculations deliver wrong results
Component@Subcomponent: MemService_AsrNvM@Implementation
First affected version: 5.00.00
Fixed in versions:
Problem Description:
What happens (symptoms):
-------------------------------------------------------------------
CRC32s calculated internally by NVM are not as specified by AUTOSAR, i.e. the results may differ, 
depending on number of single CRC library calls done per NVM block.
Calculated values are still CRCs, but they don't match the results from using corresponding 
standardized CRC32 calculations
Since CRC handling is done internally, this is usually not visible to users.
The issue becomes visible, if NVM's configuration changed between a write and a read request 
(see below): Data may become unreadable due to failed CRC check.
When does this happen:
-------------------------------------------------------------------
It happens at run-time during CRC calculation.
However this behavior is symmetric, i.e. calculated CRC during writes match the CRC calculated 
during reads. Data can be written and read back as expected.
In which configuration does this happen:
-------------------------------------------------------------------
It happens for all blocks having CRC (NvMBlockUseCrc) enabled, and CRC type (NvMBlockCrcType) 
was set to CRC32 .
If (in a running project), the number of "Bytes per MainFunction" (NvMCrcNumOfBytes) was 
changed, existing data become unreadable, because same data result in different CRC.
 
Resolution Description:
Workaround:
-------------------------------------------------------------------
In in a running project's configuration don't change the number of "Bytes per 
MainFunction" (NvMCrcNumOfBytes).
Resolution:
--------------------------------------------------------

### Page 5

Issue Report
5
ESCAN00097644 RTE dereferences NULL_PTR after execution of a 
mapped server runnable
Component@Subcomponent: Rte_Core@Implementation
First affected version: 1.13.00
Fixed in versions: 1.18.00
Problem Description:
What happens (symptoms):
-------------------------------------------------------------------
RTE dereferences a null pointer after a mapped server runnable has been executed.
This usually results in an os trap.
When does this happen:
-------------------------------------------------------------------
During runtime when a client with lower task priority calls a mapped server runnable with higher 
priority.
In which configuration does this happen:
-------------------------------------------------------------------
This happens when multiple clients are connected to the same server, and the server runnable
is mapped to a task with higher priority than at least one of the clients. This happens only for
synchronous client server communication.
 
Resolution Description:
Workaround:
-------------------------------------------------------------------
- map the server runnable to a task with lower priority than the client tasks
or
- create a proxy component that forwards the client calls to the server.
To do so a server port + server runnable is created for each client.
Each client is connected to the corresponding proxy server port.
A single proxy client port is connected to the server.
The server runnables of the proxy component calls the server through the single client port.
Resolution:
-------------------------------------------------------------------
The described issue is corrected by modification of all affected work-products.

### Page 6

Issue Report
6
ESCAN00097829 Service 0x22: Overwritten call stack
Component@Subcomponent: Diag_Asr4Dcm@Implementation
First affected version: 7.02.00
Fixed in versions: 9.03.00, 8.06.02
Problem Description:
What happens (symptoms):
-------------------------------------------------------------------
The call stack will be corrupted leading to indeterminable behavior.
The possible amount of overwritten memory depends on the largest configured DID.
After ECU reset, the no

*Excerpt: first 8 of 202 pages shown.*
