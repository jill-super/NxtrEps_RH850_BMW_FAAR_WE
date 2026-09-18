---
title: '_Bmw_5441_Eps_Impl_A — AN-ISC-8-1140_FrIf_JobListConfiguration'
description: 'Converted PDF document AN-ISC-8-1140_FrIf_JobListConfiguration.pdf from module _Bmw_5441_Eps_Impl_A.'
sidebar:
  hidden: true
---

> **Source:** `AN-ISC-8-1140_FrIf_JobListConfiguration.pdf` (PDF, 281 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 10; title: JobList Configuration of FlexRay Interface; author: Oliver, Reineke; Drescher, Markus

## Converted content

### Page 1

JobList Configuration of FlexRay Interface 
Version 1.2 
2014-03-19 
Application Note AN-ISC-8-1140 
 
 
 
Author(s) Oliver, Reineke; Drescher, Markus 
Restrictions Customer confidential - AUTOSAR only 
Abstract This application notes describes how the FlexRay Interface JobList is configured. 
 
Table of Contents 
 
 
 1 
Copyright © 2014 - Vector Informatik GmbH 
Contact Information: www.vector-informatik.com or ++49-711-80 670-0 
 
1.0 Overview .......................................................................................................................................................... 1 
1.1 What is the Job List about? ........................................................................................................................... 1 
1.1.1 Communication Jobs .................................................................................................................................. 1 
1.2 Job List Configuration .................................................................................................................................... 2 
1.2.1 Scheduling Algorithm – Default .................................................................................................................. 2 
1.2.2 Scheduling Algorithm – Concatenated Jobs ............................................................................................... 3 
1.2.3 Scheduling Algorithm – User Defined ......................................................................................................... 3 
1.3 Synchronisation of BSW main functions ....................................................................................................... 3 
2.0 Configuration aspects ...................................................................................

### Page 2

JobList Configuration of FlexRay Interface 
 
 
 
 
 2 
Application Note AN-ISC-8-1140 
 
 
According the AUTOSAR SWS the FlexRay Interface supports the following communication operations that can be 
performed for each receive or transmit buffer: 
• Decoupled Transmission 
• Receive and Indicate 
• Tx Confirmation 
 
1.2 Job List Configuration 
As the FRIF Job List configuration is difficult and error-prone, GENy offers the possibility to calculate the 
scheduling of the communication operations. The FlexRay Interface supports the following configuration 
mechanisms (SchedulingAlgorithms) in GENy: 
• Default 
• Concatenated Jobs 
• User Defined 
1.2.1 Scheduling Algorithm – Default 
The default scheduling algorithm divides the FlexRay cycle into x segments of the same size, where x is the 
number of Tx or Rx jobs. Depending on the start slot and end slot of these segments the start time of the 
corresponding task and the maximum ISR delay is automatically calculated. 
Example: 
For a cycle with a length of 5000 macro ticks which is divided into a static segment of 3000 macro ticks length and 
a dynamic segment of 2000 macro ticks length, the following segments (Segment 0 and Segment 1 in Figure 1) 
arise: 
 
 
Figure 1 – Default Scheduling Algorithm 
 
Note: A TxConf job is needed if a Tx job performs the decoupled transmission for a FlexRay frame with 
at least one PDU that shall be confirmed to the upper layer component. The Default Scheduling 
Algorithm takes the first job after the last slot of the Tx job as TxConf job. 
 In the example above Rx1 is the TxConf job for Tx1 (because it is the first job after Segment 0) and 
Rx0 is the TxConf job for Tx0 (because it is the first Job after Segment 1).

### Page 3

JobList Configuration of FlexRay Interface 
 
 
 
 
 3 
Application Note AN-ISC-8-1140 
 
 
1.2.2 Scheduling Algorithm – Concatenated Jobs 
In contrast to the default algorithm the Concatenated Jobs algorithm configures the start time of an Rx and the 
following Tx FRIF job to the same macrotick parameter and enables the Job Concatenation Enable option. As one 
timer interrupt is used to activate an Rx and Tx FRIF job, this algorithm can be used to reduce the interrupt load of 
the FlexRay Interface. 
 
Figure 2 – Concatenated Jobs Scheduling Algorithm 
 
Note: Due to the job concatenation it is not possible to achieve both shortest possible indication times 
after reception and latest data for transmission. 
 
For example in the picture above the concatenated jobs Rx0 and Tx0 can either be placed at the 
beginning of the cycle with the consequence that the data indications for frames in Segment 1 will 
be given to the upper layer components as soon as possible. Or Rx0 and Tx0 can be placed just 
before the start of Segment 1 to reduce the age of the transmitted data. 
 
1.2.3 Scheduling Algorithm – User Defined 
Beside the automated job placement GENy offers the possibility to configure the following job parameters 
manually: 
• Start Slot and End Slot (or assignment of single frames to a Job) 
• Macrotick 
• Maximum permissible ISR delay 
• TxConf Job 
 
1.3 Synchronisation of BSW main functions 
For deterministic communication behaviour on FlexRay it is necessary to synchronize the main function of FlexRay 
relevant BSW modules to the global time of the FlexRay CC. If the main functions are not synchronized it is 
possible that obsolete data is received or updated PDUs are not transmitted during the FlexRay cycle. 
 
For example if an application task shall receive P

### Page 4

JobList Configuration of FlexRay Interface 
 
 
 
 
 4 
Application Note AN-ISC-8-1140 
 
 
 
Figure 3 – Unsynchronized application behaviour on FlexRay 
 
There are several ways to synchronize BSW modules to the FlexRay global time: 
1. Using synchronized schedule tables of the AUTOSAR OS 
2. Cancel and set relative alarms in the FlexRay timer or cycle start ISR (like the MICROSA R SCHM does) 
3. Calling the BSW main function directly in the context of the FlexRay timer or cycle start ISR 
 
Note: Calling the BSW main function only in the context of the FlexRay timer or cycle start ISR has the 
disadvantage that the main function won’t be called if the FlexRay bus loses synchronization. 
2.0 Configuration aspects 
For optimal BSW behaviour some configuration aspects shall be considered by the integrator as described in this 
section. Using the example of FRTP this chapter explains the details of: 
• FRIF job placement and configuration 
• Main function placement 
• FRIF PDU settings 
• Task priorities and interruptibilities 
• Duration of critical sections or resource locks 
• SystemTimer tick time 
 
Note: These settings are also relevant for non-FRTP modules like COM, PDUR, FRNM and FRXCP 
 
Note: Some FRNM specific details are also provided where applicable. 
In the following example the FRTP PDUs are all transmitted and received during the dynamic segment of the 
FlexRay cycle as depicted below. The corresponding frames have a cycle repetition 1 (meaning that they could be 
sent every cycle). 
 
Note: With AUTOSAR 3.2.2 FRTP only the last Tx PDU of a PDU pool is confirmed by the FlexRay 
Interface to reduce the CPU and interrupt load.

### Page 5

JobList Configuration of FlexRay Interface 
 
 
 
 
 5 
Application Note AN-ISC-8-1140 
 
 
 
2.1 PDUs with decoupled transmission 
If FRTP PDUs are configured to use decoupled transmission, the transmission rate of the FlexRay Transport Layer 
strongly depends on the positioning of the FRTP main function and the Rx, Tx and TxConf FRIFJobs of the FRTP 
frames. 
Note: If the FRTP PDUs are sent with immediate transmission (the message buffers are written in the 
context of the FRTP main function) only the start times of the Rx and TxConf jobs are relevant for 
the placement of the FRTP main function. 
2.1.1 Optimal BSW main function placement 
2.1.1.1 FRTP Main Function placement 
To achieve optimal throughput for segmented TP transmission it is recommended to place the SCHM Task which 
executes the FRTP main function between the Rx and the Tx FRIFJob of the TP frames. The Rx FRIFJob should 
handle the TxConfirmation as de

*Excerpt: first 8 of 10 pages shown.*
