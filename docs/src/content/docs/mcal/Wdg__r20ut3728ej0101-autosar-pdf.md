---
title: 'Wdg — R20UT3728EJ0101-AUTOSAR'
description: 'Converted PDF document R20UT3728EJ0101-AUTOSAR.pdf from module Wdg.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3728EJ0101-AUTOSAR.pdf` (PDF, 910 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 60; title: AUTOSAR MCALR4.0 User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

AUTOSAR MCAL R4.0.3 
User’s Manual 
 
 
 
 
WDG Driver Component Ver.1.0.8 
 
Embedded User’s Manual 
 
 
 
 
 
Target Device: 
RH850/P1x 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
 
www.renesas.com Rev.1.01 Feb 2017

### Page 2

2

### Page 3

3 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Notice 
1. Descriptions of circuits, software and other related information in this document are provided only to illustrate the operation of 
semiconductor products and application examples. You are fully responsible for the incorporation or any other use of the circuits, 
software, and information in the design of your product or system. Renesas Electronics disclaims any and all liability for any losses and 
damages incurred by you or third parties arising from the use of these circuits, software, or information. 
2. Renesas Electronics hereby expressly disclaims any warranties against and liability for infringement or any other disputes involving patents, 
copyrights, or other intellectual property rights of third parties, by or arising from the use of Renesas Electronics products or technical information 
described in this document, including but not limited to, the product data, drawing, chart, program, algorithm, application examples. 
3. No license, express, implied or otherwise, is granted hereby under any patents, copyrights or other intellectual property rights of Renesas 
Electronics or others. 
4. You shall not alter, modify, copy, or otherwise misappropriate any Renesas Electronics product, whether in whole or in part. Renesas Electronics 
disclaims any and all liability for any losses or damages incurred by you or third parties arising from such alteration, modification, copy or 
otherwise misappropriation of Renesas Electronics products. 
5. Renesas Electronics products are classified according to the following two quality grades: "Standard" and "High Quality". The intended 
applications for each Re

### Page 4

4

### Page 5

5 
Abbreviations and Acronyms 
 
Abbreviation / Acronym Description 
ADC Analog Digital Converter 
ANSI American National Standards Institute 
API Application Programming Interface 
AUTOSAR Automotive Open System ARchitecture 
ARXML AUTOSAR Markup EXtensible Language 
BSW Basic SoftWare 
CAN Controller Area Network 
DEM Diagnostic Event Manager 
DET/Det Development Error Tracer 
DIO Digital Input And Output 
ECU Electronic Control Unit 
EEPROM Electrical Erasable Programmable Read Only Memory 
FR FlexRay 
GHS Green HillS 
GNU GNU is Not Unix 
GPT General Purpose Timer 
HW HardWare 
ID/Id Identifier 
ISR Interrupt Service Routine 
IMR Interrupt Mask Register 
I/O Input/Output 
ICU Input Capture Unit 
INTWDTn Interrupt Watch Dog Timer. 
LIN Local Interconnect Network 
MCAL Microcontroller Abstraction Layer 
MCU MicroController Unit 
MHz Mega Hertz 
OS Operating System 
PWM Pulse Width Modulation 
PDF Parameter Definition File 
RAM Random Access Memory 
ROM Read Only Memory 
RTE Run Time Environment 
SCI Serial Communication Interface 
SPI Serial Peripheral Interface 
 SCHM/SchM Scheduler Manager 
 SV Supervisor Mode 
 SW SoftWare 
WDG/wdg WatchDog 
WDT WatchDog Timer 
WDGIF WatchDog Interface

### Page 6

6 
WDTAnTRES WatchDog Timer A Trigger Reset 
WDTATCKI WatchDog Timer A Trigger Clock Input 
WDTAnMD WatchDog Timer Mode 
WDTAnREF Watch Dog Timer A Reference 
 
 
Definitions 
 
Term Represented by 
Sl. No. Serial Number 
WDTAEVAC Watchdog Timer Enable Register for Varying Activation Code 
WDTAMD Watchdog Timer Mode Register 
WDTAWDTE Watchdog Timer Enable Register for Fixed Activation Code

### Page 7

7 
Table of Contents 
 
Chapter 1 Introduction ..................................................................... 11 
1.1. Document Overview ........................................................................................................... 13 
Chapter 2 Reference Documents ..................................................... 15 
Chapter 3 Integration And Build Process ....................................... 17 
3.1. WDG Driver Component Makefile ..................................................................................... 17 
3.1.1. Folder Structure.................................................................................................... 17 
Chapter 4 Forethoughts ................................................................... 19 
4.1. General ................................................................................................................................. 19 
4.2. Preconditions ...................................................................................................................... 20 
4.3. Data Consistency ................................................................................................................ 20 
4.4. WDG State Diagram ............................................................................................................ 21 
4.5. WDTA 75% ISR Usage Details for R4.0.3 .......................................................................... 22 
4.6. Deviation List ...................................................................................................................... 24 
4.7. User mode and supervisor mode ...................................................................................... 25 
4.8. Register Write Verify ..........................................

### Page 8

8 
Chapter 11 Development And Production Errors ............................. 43 
11.1. WDG Driver Component Development Errors ................................................................. 43 
11.2. WDG Driver Component Production Errors ..................................................................... 44 
Chapter 12 Memory Organization ...................................................... 45 
Chapter 13 P1M Specific Information ................................................ 47 
13.1. Interaction Between The User And WDG Driver Component .......................................... 47 
13.1.1. ISR Function Mapping Interrupt Vector Table ...................................................... 47 
13.1.2. Translation Header File ........................................................................................ 47 
13.1.3. Parameter Definition File ...................................................................................... 48 
13.2. Sample Application............................................................................................................. 48 
13.2.1 Sample Application Structure ............................................................................... 48 
13.2.2 Building Sample Application ................................................................................. 50 
13.2.2.1 Configuration Example ..................................................................... 50 
13.2.2.2 Debugging The Sample Application ................................................. 50 
13.3. Memory and Throughput for R4.0.3 .................................................................................. 51 
13.3.1 ROM/RAM Usage ................................................................................................ 51 
13.3.2 S

*Excerpt: first 8 of 60 pages shown.*
