---
title: 'Xcp — XCP_ReferenceBook_V3.0_EN'
description: 'Converted PDF document XCP_ReferenceBook_V3.0_EN.pdf from module Xcp.'
sidebar:
  hidden: true
---

> **Source:** `XCP_ReferenceBook_V3.0_EN.pdf` (PDF, 4624 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 116; title: XCP – The Standard Protocol for ECU Development; author: Vector Informatik GmbH: Andreas Patzer | Rainer Zaiser

## Converted content

### Page 1

Andreas Patzer | Rainer Zaiser
XCP – The Standard Protocol
for ECU Development
Fundamentals and Application Areas

### Page 2

Andreas Patzer | Rainer Zaiser
XCP – The Standard Protocol for ECU Development

### Page 3

Date December 2016
Reproduction only with expressed permission from 
Vector Informatik GmbH, Ingersheimer Str. 24, 70499 Stuttgart, Germany
© 2016 by Vector Informatik GmbH. All rights reserved. This book is only intended for personal use, but not 
for technical or commercial use. It may not be used as a basis for contracts of any kind. All information in this 
book was compiled with the greatest possible care, but Vector Informatik does not assume any guarantee or 
warranty whatsoever for the correctness of the information it contains. The liability of Vector Informatik is 
excluded, except for malicious intent or gross negligence, to the extent that laws do not make it legally liable. 
 
Information contained in this book may be protected by copyright and / or patent rights. Product names of 
software, hardware and other product names that are used in this book may be registered brands or otherwise 
protected by branding laws, regardless of whether or not they are identified as registered brands.

### Page 4

XCP
The Standard Protocol
for ECU Development
Fundamentals and Application Areas
Andreas Patzer, Rainer Zaiser 
Vector Informatik GmbH

### Page 5

Table of Contents
Introduction ........................................................................................................................................... 7
1 Fundamentals of the XCP Protocol ........................................................................................... 13
1.1 XCP Protocol Layer ................................................................................................................ 19
 1.1.1 Identification Field ........................................................................................................21
 1.1.2 Timestamp .....................................................................................................................21
 1.1.3 Data Field ......................................................................................................................22
1.2 Exchange of CTOs .................................................................................................................. 22
 1.2.1 XCP Command Structure ..........................................................................................22
 1.2.2 CMD ................................................................................................................................25
 1.2.3 RES ..................................................................................................................................28
 1.2.4 ERR ..................................................................................................................................28
 1.2.5 EV .................................................................................................................................... 29
 1.2.6 SERV ..................................................................................................

### Page 6

2 ECU Description File A2L ............................................................................................................. 71
2.1 Setting Up an A2L File for an XCP Slave ......................................................................... 74
2.2 Manually Creating an A2L File ............................................................................................ 75
2.3 A2L Contents versus ECU Implementation ..................................................................... 76
3 Calibration Concepts ................................................................................................................... 79
3.1 Parameters in Flash .............................................................................................................. 80
3.2 Parameters in RAM ................................................................................................................ 82
3.3 Flash Overlay ...........................................................................................................................84
3.4 Dynamic Flash Overlay Allocation ..................................................................................... 85
3.5 RAM Pointer Based Calibration Concept per AUTOSAR .............................................86
 3.5.1 Single Pointer Concept ...............................................................................................86
 3.5.2 Double Pointer Concept .............................................................................................88
3.6 Flash Pointer Based Calibration Concept ....................................................................... 89
4 Application Areas of XCP .......................................................................................................

### Page 7

7
Introduction
Introduction
In optimal parameterization (calibration) of electronic ECUs, you calibrate parameter values 
during the system runtime and simultaneously acquire measured signals. The physical con­
nection between the development tool and the ECU is via a measurement and calibration 
protocol. XCP has become established as a standard here.
First, the fundamentals and mechanisms of XCP will be explained briefly and then the appli­
cation areas and added value for ECU calibration will be discussed.
First, some facts about XCP:
> XCP signifies “Universal Measurement and Calibration Protocol”. The “X” stands for the 
variable and interchangeable transport layer.
> It was standardized by an ASAM working committee (Association for Standardisation of 
Automation and Measuring Systems). ASAM is an organization of automotive OEMs, sup­
pliers and tool producers.
> XCP is the protocol that succeeds CCP (CAN Calibration Protocol).
> The conceptual idea of the CAN Calibration Protocol was to permit read and write access 
to internal ECU data over CAN. XCP was developed to implement this capability via dif ­
ferent transmission media. Then one speaks of XCP on CAN, XCP on FlexRay or XCP on 
Ethernet. 
> The primary applications of XCP are measurement and calibration of internal ECU para­
meters. Here, the protocol offers the ability to acquire measured values “event synchro­
nous” to processes in ECUs. This ensures consistency of the data between one another.
To visualize the underlying idea, we initially view the ECU and the software running in it as a 
black box. In a black box, only the inputs into the ECU (e.g. CAN messages and sensor values) 
and the output from the ECU (e.g. CAN messages and actuator drives) are acquired. Details 
about the internal processing of 

### Page 8

8
 Introduction
and all of this at model runtime or retrospectively after a time­limited test run has been 
completed. A write access is needed if parameterizations are changed, e.g. if the propor ­
tional component of a PID controller is modified to adapt the algorithm behavior to the 
 system under control. Regardless of where your application runs – focal points are always 
the detailed analysis of algorithm processes and optimization by changes to the 
parameterization.
This generalization can be made: The algorithms may exist in any type of executable form 
(code or model description). Different systems may be used as the runtime environment 
(Simulink, as DLL on the PC, on a rapid prototyping platform, in the ECU etc.). Process flows 
are analyzed by read access to data and acquisition of its time­based flow. Parameter sets 
are modified iteratively to optimize algorithms. To simplify the representation, the acquisi­
tion of data can be externalized to an external PC­based tool, although it is understood here 
that runtime environments themselves can even offer analysis capabilities.
Figure 1: 
Fundamental 
communication with 
a

*Excerpt: first 8 of 116 pages shown.*
