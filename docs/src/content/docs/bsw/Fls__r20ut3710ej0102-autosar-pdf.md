---
title: 'Fls — R20UT3710EJ0102-AUTOSAR'
description: 'Converted PDF document R20UT3710EJ0102-AUTOSAR.pdf from module Fls.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3710EJ0102-AUTOSAR.pdf` (PDF, 1348 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 82; title: AUTOSAR MCAL  R4.0  User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

AUTOSAR MCAL R4.0.3 
User's Manual 
FLS Driver Component Ver.1.0.5 
Embedded User's Manual Target Device: 
RH850/P1x 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
www.renesas.com Rev.1.02 May 2017

### Page 2

2

### Page 3

3 
 
Notice 
1. Descriptions of circuits, software and other related information in this document are provided only to illustrate the operation of 
semiconductor products and application examples. You are fully responsible for the incorporation or any other use of the 
circuits, software, and information in the design of your product or system. Renesas Electronics disclaims any and all liability 
for any losses and damages incurred by you or third parties arising from the use of these circuits, software, or information. 
2. Renesas Electronics hereby expressly disclaims any warranties against and liability for infringement or any other disputes involving 
patents, copyrights, or other intellectual property rights of third parties, by or arising from the use of Renesas Electronics products or 
technical information described in this document, including but not limited to, the product data, drawing, chart, program, algorithm, 
application examples. 
3. No license, express, implied or otherwise, is granted hereby under any patents, copyrights or other intellectual property rights of 
Renesas Electronics or others. 
4. You shall not alter, modify, copy, or otherwise misappropriate any Renesas Electronics product, whether in whole or in part. Renesas 
Electronics disclaims any and all liability for any losses or damages incurred by you or third parties arising from such alteration, 
modification, copy or otherwise misappropriation of Renesas Electronics products. 
5. Renesas Electronics products are classified according to the following two quality grades: "Standard" and "High Quality". The intended 
applications for each Renesas Electronics product depends on the product’s quality grade, as indicated below. 
"Standard": Computers; office equipment; communications equipment;

### Page 4

4

### Page 5

5 
Abbreviations and Acronyms 
 
 
 
Abbreviation / Acronym Description 
 ANSI American National Standards Institute 
 ADC Analog to Digital Converter 
 API Application Programming Interface 
 AUTOSAR AUTomotive Open System ARchitecture 
 BSW Basic SoftWare 
 BSWMDT Basic Software Module Description Template 
 BUS Bidirectional Universal Switch 
 CPU Central Processing Unit 
 CAN Controller Area Network 
 DET/Det Development Error Tracer 
 DEM/Dem Diagnostic Event Manager 
 DIO Digital Input Output 
 DMA Direct Memory Access 
 DED Double bit Error Detection 
 EEPROM Electrically Erasable Programmable Read Only Memory 
 ECU Electronic Control Unit 
 ECC Error Correction Code 
 FACI Flash Application Command Interface 
 FCU Flash Control Unit 
 FLS FLaSh Driver 
 GPT General Purpose Timer 
 GNU GNU’s Not Unix 
 HW HardWare 
 ID/Id Identifier 
 IO InOut 
 ICU Input Capture Unit 
 I/O Input/Output 
 ISR Interrupt Service Routine 
 KB Kilo Byte 
 LIN Local Interconnect Network 
 MB Mega Byte 
 MHz Mega Hertz 
 MCU Micro Controller Unit 
 MCAL Microcontroller Abstraction Layer 
 NA Not Applicable 
 OS Operating System 
 PDF Parameter definition file 
 PWM Pulse Width Modulation 
 RAM Random Access Memory

### Page 6

6 
Abbreviation / Acronym Description 
 ROM Read Only Memory 
 R/W/RW Read/Write/Read and Write 
 RTE Run Time Environment 
 SCHM/SchM Scheduler Manager 
 SCI Serial Communications Interface 
 SPI Serial Peripheral Interface 
 SED Single bit Error Detection 
 SW SoftWare 
 WDT Watch Dog Timer 
 
 
 
Definitions 
 
 
 
Term Represented by 
Sl. No. Serial Number

### Page 7

7 
Table of Contents 
 
 
Chapter 1 Introduction....................................................................... 11 
1.1 Document Overview ........................................................................................................... 13 
Chapter 2 Reference Documents ...................................................... 15 
Chapter 3 Integration and Build Process ......................................... 17 
3.1. FLS Driver Component Make file ...................................................................................... 17 
3.1.1. Folder Structure ................................................................................................. 17 
Chapter 4 Forethoughts .................................................................... 19 
4.1. General ................................................................................................................................. 19 
4.2. Preconditions ...................................................................................................................... 22 
4.3. Data Consistency ................................................................................................................ 25 
4.4. Deviation List ...................................................................................................................... 27 
4.5. User mode and supervisor mode ...................................................................................... 28 
Chapter 5 Architecture Details .......................................................... 29 
Chapter 6 Registers Details ............................................................... 35 
Chapter 7 Interaction between the User and FLS Driver Component 
 .................................................................

### Page 8

8 
10.3.5. Fls_GetStatus ..................................................................................................... 51 
10.3.6. Fls_GetJobResult ............................................................................................... 52 
10.3.7. Fls_MainFunction ............................................................................................... 52 
10.3.8. Fls_Read ............................................................................................................. 53 
10.3.9. Fls_Compare....................................................................................................... 53 
10.3.10. Fls_SetMode ....................................................................................................... 54 
10.3.11. Fls_GetVersionInfo ............................................................................................ 54 
10.3.12. Fls_ReadImmediate ........................................................................................... 55 
10.3.13. Fls_BlankCheck ................................................................................................. 55 
10.3.14. Fls_Suspend ....................................................................................................... 56 
10.3.15. Fls_Resume ........................................................................................................ 57 
10.3.16. Fls_CallSwitchBFlashErrorNotification ........................................................... 57 
Chapter 11 Development and Production Errors ............................. 59 
11.1 FLS Driver Component Development Errors ................................................................... 59 
11.2 FLS Driver Component Production Errors .................................................

*Excerpt: first 8 of 82 pages shown.*
