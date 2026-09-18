---
title: 'RenesasMcalSuprt — R20UT3827EJ0100-AUTOSAR'
description: 'Converted PDF document R20UT3827EJ0100-AUTOSAR.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3827EJ0100-AUTOSAR.pdf` (PDF, 822 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 50; title: AUTOSAR_ Modules_Overview; author: Renesas Electronics Corporation

## Converted content

### Page 1

AUTOSAR Modules Overview 
User’s Manual 
 
 
 
 
Version 1.0.2 
 
 
 
Target Device: 
RH850/X1x 
 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
 
 
 
 
Renesas Electronics 
www.renesas.com Rev.1.00 Nov 2016

### Page 2

2

### Page 3

3 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
2 
Notice 
1. All information included in this document is current as of the date this document is issued. Such information, however, is 
subject to change without any prior notice. Before purchasing or using any Renesas Electronics products listed herein, please 
confirm the latest product information with a Renesas Electronics sales office. Also, please pay regular and careful attention to 
additional and different information to be disclosed by Renesas Electronics such as that disclosed through our website. 
2. Renesas Electronics does not assume any liability for infringement of patents, copyrights, or other intellectual property rights of 
third parties by or arising from the use of Renesas Electronics products or technical information described in this document. No 
license, express, implied or otherwise, is granted hereby under any patents, copyrights or other intellectual property rights of 
Renesas Electronics or others. 
3. You should not alter, modify, copy, or otherwise misappropriate any Renesas Electronics product, whether in whole or in part. 
4. Descriptions of circuits, software and other related information in this document are provided only to illustrate the operation of 
semiconductor products and application examples. You are fully responsible for the incorporation of these circuits, software, 
and information in the design of your equipment. Renesas Electronics assumes no responsibility for any losses incurred by 
you or third parties arising from the use of these circuits, software, or information. 
5. When exporting the products or technology described in this document, you should comply with

### Page 4

4

### Page 5

5 
Abbreviations and Acronyms 
 
 
 
Abbreviation / Acronym Description 
ADC Analog to Digital Converter 
API Application Programming Interface 
ANSI American National Standards Institute 
ATOM ARU-connected Timer Output Module 
AUTOSAR AUTomotive Open System ARchitecture 
CC Communication Controller 
CMU Clock Management Unit 
CORTST Core Test 
DEM Diagnostic Event Manager 
DET/Det Development Error Tracer 
DIO Digital Input Output 
ETH Ethernet 
FLS FLaSh Driver 
FLSTST FLaSh Test 
FR FlexRay 
FSL Flash Self programming Library 
GPT General Purpose Timer 
GTM Generic Timer Module 
ICU Input Capture Unit 
LIN Local Interconnect Network 
LPdu/Lpdu Data Link Protocol Datagram Unit 
MCAL MicroController Abstraction Layer 
MCU MicroController Unit 
Nm Network Management 
POC Protocol Operation Control 
PWM Pulse Width Modulation 
RAMTST Ram Test 
Rx Receiver 
SPI Serial Peripheral Interface 
TIM Timer Input Module 
Tx Transmitter 
WDG WatchDog driver 
 
 
 
Definitions 
 
 
 
Term Represented by 
Sl. No. Serial Number 
<Autosar Version> 4.0.3 when tested for R4.0.3

### Page 6

6

### Page 7

7 
Table of Contents 
 
Chapter 1 INTRODUCTION ............................................................................................. 11 
1.1. Document Overview ........................................................................................................ 12 
Chapter 2 REFERENCE DOCUMENTS .......................................................................... 13 
Chapter 3 AUTOSAR MODULES .................................................................................... 15 
3.1 MCAL Module .................................................................................................................. 15 
3.1.1. ADC Driver Component .................................................................................... 15 
3.1.1.1. Module Overview .............................................................................15 
3.1.1.2. Module Dependency........................................................................16 
3.1.1.3. Configuration Parameter Dependency ............................................16 
3.1.1.4. Source Code Dependency ..............................................................16 
3.1.1.5. Stubs ...............................................................................................17 
3.1.2. PWM Driver Component ................................................................................... 17 
3.1.2.1. Module Overview .............................................................................17 
3.1.2.2. Module Dependency........................................................................18 
3.1.2.3. Configuration Parameter Dependency ............................................18 
3.1.2.4. Source Code Dependency ..............................................................18 
3.1.2.5. Stubs ......

### Page 8

8 
3.1.7.5. Stubs ...............................................................................................28 
3.1.8. MCU Driver Component.................................................................................... 28 
3.1.8.1. Module Overview .............................................................................28 
3.1.8.2. Module Dependency .......................................................................28 
3.1.8.3. Configuration Parameter Dependency ...........................................29 
3.1.8.4. Source Code Dependency ..............................................................29 
3.1.8.5. Stubs ...............................................................................................29 
3.1.9. GPT Driver Component .................................................................................... 30 
3.1.9.1. Module Overview .............................................................................30 
3.1.9.2. Module Dependency........................................................................30 
3.1.9.3. Configuration Parameter Dependency ............................................31 
3.1.9.4. Source Code Dependency ..............................................................31 
3.1.9.5. Stubs ...............................................................................................32 
3.1.10. WDG Driver Component ................................................................................... 32 
3.1.10.1. Module Overview .............................................................................32 
3.1.10.2. Module Dependency........................................................................32 
3.1.10.3. Configuration Parameter Dependency ............................................33 
3.1.10.

*Excerpt: first 8 of 50 pages shown.*
