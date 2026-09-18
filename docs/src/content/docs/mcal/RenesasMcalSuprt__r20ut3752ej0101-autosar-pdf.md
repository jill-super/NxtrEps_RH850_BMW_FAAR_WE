---
title: 'RenesasMcalSuprt — R20UT3752EJ0101-AUTOSAR'
description: 'Converted PDF document R20UT3752EJ0101-AUTOSAR.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3752EJ0101-AUTOSAR.pdf` (PDF, 818 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 48; title: AUTOSAR Modules Overview User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

AUTOSAR Modules Overview 
User’s Manual 
 
 
 
 
Version 1.0.10 
 
 
 
Target Device: 
RH850/P1x 
 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
 
 
 
 
Renesas Electronics 
www.renesas.com Rev.1.01 Feb 2017

### Page 2

2

### Page 3

3 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
2 
 
 
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
applications for 

### Page 4

4

### Page 5

5 
 
 
 
 
Abbreviations and Acronyms 
 
 
 
Abbreviation / Acronym Description 
ADC Analog to Digital Converter 
API Application Programming Interface 
ANSI American National Standards Institute 
AUTOSAR AUTomotive Open System ARchitecture 
CAN Controller Area Network 
DEM Diagnostic Event Manager 
DET/Det Development Error Tracer 
DIO Digital Input Output 
FEE Flash EEPROM Emulation 
FLS FLaSh Driver 
FSL Flash Self programming Library 
FR Flex-Ray 
GPT General Purpose Timer 
ICU Input Capture Unit 
LIN Local Interconnect Network 
MCAL MicroController Abstraction Layer 
MCU MicroController Unit 
PWM Pulse Width Modulation 
SPI Serial Peripheral Interface 
TAU Timer Array Unit 
WDG WatchDog driver 
 
 
 
Definitions 
 
 
Term Represented by 
Sl. No. Serial Number

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
3.1.1.5. Stubs ...............................................................................................16 
3.1.2. PWM Driver Component ................................................................................... 17 
3.1.2.1. Module Overview .............................................................................17 
3.1.2.2. Module Dependency........................................................................18 
3.1.2.3. Configuration Parameter Dependency ............................................18 
3.1.2.4. Source Code Dependency ..............................................................18 
3.1.2.5. Stubs ....

### Page 8

8 
 
3.1.7.4. Source Code Dependency ..............................................................25 
3.1.7.5. Stubs ...............................................................................................26 
3.1.8. ICU Driver Component...................................................................................... 26 
3.1.8.1. Module Overview .............................................................................26 
3.1.8.2. Module Dependency .......................................................................27 
3.1.8.3. Configuration Parameter Dependency ...........................................28 
3.1.8.4. Source Code Dependency ..............................................................28 
3.1.8.5. Stubs ...............................................................................................28 
3.1.9. MCU Driver Component.................................................................................... 29 
3.1.9.1. Module Overview .............................................................................29 
3.1.9.2. Module Dependency .......................................................................29 
3.1.9.3. Configuration Parameter Dependency ...........................................30 
3.1.9.4. Source Code Dependency ..............................................................30 
3.1.9.5. Stubs ...............................................................................................30 
3.1.10. GPT Driver Component .................................................................................... 30 
3.1.10.1. Module Overview .............................................................................30 
3.1.10.2. Module Dependency........................................................................31 

*Excerpt: first 8 of 48 pages shown.*
