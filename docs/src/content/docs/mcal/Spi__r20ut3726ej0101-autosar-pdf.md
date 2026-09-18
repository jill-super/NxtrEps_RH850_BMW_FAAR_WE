---
title: 'Spi — R20UT3726EJ0101-AUTOSAR'
description: 'Converted PDF document R20UT3726EJ0101-AUTOSAR.pdf from module Spi.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3726EJ0101-AUTOSAR.pdf` (PDF, 1476 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 96; title: AUTOSAR MCAL R4.0 User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

AUTOSAR MCAL R4.0.3 
User’s Manual 
 
 
 
 
 
SPI Driver Component Ver.1.0.12 
Embedded User’s Manual 
 
 
Target Device: 
RH850/P1x 
 
 
 
 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
www.renesas.com Rev.1.01 Mar 2017

### Page 2

2

### Page 3

3 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
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
applications for each Renes

### Page 4

4

### Page 5

5 
Abbreviations and Acronyms 
 
Abbreviation / Acronym Description 
ANSI American National Standards Institute 
API Application Programming Interface 
ARXML/arxml AutosaR eXtensible Mark-up Language 
ASIC Application Specific Integration Circuit 
AUTOSAR AUTomotive Open System Architecture 
BSW Basic SoftWare 
CPU Central Processing Unit 
CS Chip Select 
CSIH/CSIG Enhanced Queued Clocked Serial Interface. 
DEM/Dem Diagnostic Event Manager 
DET/Det Development Error Tracer 
DMA Direct Memory Access 
EB External Buffer 
ECU Electronic Control Unit 
EEPROM Electrically Erasable Programmable Read-Only Memory 
FIFO First In First Out 
GNU GNU’s Not Unix 
GPT General Purpose Timer 
HW HardWare 
IB Internal Buffer 
Id Identifier 
I/O Input/Output 
ISR Interrupt Service Routine 
MCAL Microcontroller Abstraction Layer 
MHz Mega Hertz 
MCU Microcontroller unit 
NA Not Applicable 
PLL Phase Locked Loop 
RAM Random Access Memory 
ROM Read Only Memory 
RTE Run Time Environment 
SPI Serial Peripheral Interface 
PDF Parameter Definition File 
DIO Digital Input Output 
WDT Watchdog Timer 
RUCG Renesas Unified Code Generator 
μC Micro controller 
XML eXtensible Mark-up Language 
ICU Input Capture Unit 
CAN Controller Area Network 
BUS BUS Network

### Page 6

6 
PWM Pulse Width Modulation 
PORT Represents a whole configurable port on a microcontroller device 
ADC Analog to Digital Converter 
LIN Local Interconnect Network 
 
 Definitions 
 
Term Represented by 
Sl. No. Serial Number

### Page 7

7 
Table Of Contents 
 
Chapter 1 Introduction ....................................................................... 11 
1.1. Document Overview ................................................................................................................ 13 
Chapter 2 Reference Documents ...................................................... 15 
Chapter 3 Integration And Build Process ......................................... 17 
3.1. SPI Driver Component Makefile ............................................................................................. 17 
Chapter 4 Forethoughts ..................................................................... 19 
4.1. General...................................................................................................................................... 19 
4.2. Preconditions ........................................................................................................................... 27 
4.3. User Mode and Supervisor Mode ........................................................................................... 28 
4.4. Memory modes ........................................................................................................................ 29 
4.5. Data Consistency ..................................................................................................................... 30 
4.6. Deviation List ........................................................................................................................... 31 
Chapter 5 Architecture Details .......................................................... 33 
Chapter 6 Registers Details ............................................................... 37 
Chapter 7 Interaction Between The User And SPI Driver Component 
 ............

### Page 8

8 
 Spi_HWUnitType ....................................................................................................... 59 
 Spi_AsyncModeType ................................................................................................. 59 
 Spi_CommErrorType ................................................................................................. 59 
 Spi_HWErrorsType .................................................................................................... 60 
 Spi_SelfTestType ...................................................................................................... 60 
 Spi_ReturnStatus ....................................................................................................... 60 
10.3 Function Definitions ....................................................................................................................... 61 
10.3.1 Spi_Init ........................................................................................................................ 61 
10.3.2 Spi_DeInit .................................................................................................................... 62 
10.3.3 Spi_WriteIB ................................................................................................................. 62 
10.3.4 Spi_AsyncTransmit ..................................................................................................... 63 
10.3.5 Spi_ReadIB ................................................................................................................. 63 
10.3.6 Spi_SetupEB ............................................................................................................... 64 
10.3.7 Spi_GetStatus ...................................................................

*Excerpt: first 8 of 96 pages shown.*
