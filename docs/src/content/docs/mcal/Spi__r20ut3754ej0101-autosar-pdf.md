---
title: 'Spi — R20UT3754EJ0101-AUTOSAR'
description: 'Converted PDF document R20UT3754EJ0101-AUTOSAR.pdf from module Spi.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3754EJ0101-AUTOSAR.pdf` (PDF, 503 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 44; title: RUCG Tool User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

RUCG Tool 
User’s Manual 
 
 
 
 
Version 1.1.3 
 
 
 
 
 
 
Target Device: 
RH850/P1M 
 
 
 
 
 
 
 
 
 
 
 
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
software, and information in the design of your product or system. Renesas Electronics disclaims any and all liability for any losses 
and damages incurred by you or third parties arising from the use of these circuits, software, or information. 
2. Renesas Electronics hereby expressly disclaims any warranties against and liability for infringement or any other disputes involving patents, 
copyrights, or other intellectual property rights of third parties, by or arising from the use of Renesas Electronics products or technical 
information described in this document, including but not limited to, the product data, drawing, chart, program, algorithm, application 
examples. 
3. No license, express, implied or otherwise, is granted hereby under any patents, copyrights or other intellectual property rights of Renesas 
Electronics or others. 
4. You shall not alter, modify, copy, or otherwise misappropriate any Renesas Electronics product, whether in whole or in part. Renesas 
Electronics disclaims any and all liability for any losses or damages incurred by you or third parties arising from such alteration, 
modification, copy or otherwise misappropriation of Renesas Electronics products. 
5. Renesas Electronics products are classified according to the following two quality grades: "Standard" and "High Quality". The intended 
applications for each Renesas Electronics product depends on the product’s quality grade, as indicated below. 
"Standard": Computers; office equipment; communications equi

### Page 4

4

### Page 5

5 
 
 
 Abbreviations and Acronyms 
 
 
 
Abbreviation / Acronym Description 
ARXML/arxml AUTOSAR xml 
AUTOSAR AUTomotive Open System Architecture 
BSWMDT Basic Software Module Description Template 
<MSN> Module Short Name 
ECU Electronic Control Unit 
DMA Direct Memory Access 
ECU Electronic Control Unit 
MCAL Microcontroller Abstraction Layer 
MCU Microcontroller Unit 
XML eXtensible Mark-up Language 
DLL Dynamic Linking Library 
 
 
 
Definitions 
 
 
 
Terminology Description 
.arxml AUTOSAR XML File. 
.trxml Translation XML File. 
PerlCtrl The utility converts a Perl program into an ActiveX control.

### Page 6

6

### Page 7

7 
 
Table of Contents 
 
Chapter 1 Introduction .........................................................................9 
1.1 Document Overview ............................................................................................................... 9 
Chapter 2 Reference ........................................................................... 11 
2.1. Reference Documents.......................................................................................................... 11 
2.2. Trademark Notice ................................................................................................................ 11 
Chapter 3 Tool Overview ..................................................................... 13 
3.1 Usage..................................................................................................................................... 13 
Chapter 4 Input Files .......................................................................... 17 
4.1 Msn Control DLL .................................................................................................................. 17 
4.2 ECU Configuration Description File(s) .............................................................................. 17 
4.3 BSWMDT File ........................................................................................................................ 17 
4.4 Translation XML File ............................................................................................................ 18 
4.4.1 Translation Header File ............................................................................................. 18 
4.4.2 Device Specific Header File ...................................................................................... 18 
4.5 Configuration XML 

### Page 8

8 
 
List of Figures 
 
Figure 3.1 Tool Overview ........................................................................................................................ 13 
 
 
 
 
 
List of Tables 
 
Table 1.1 Document Overview .................................................................................................................. 9 
Table 2.1 Reference Documents .............................................................................................................. 11 
Table 3.1 Options and Description ........................................................................................................ 14 
Table 8.1 R3.2.2 BSWMDT Mandatory Parameters .............................................................................. 32 
Table 8.2 R4.0.3 BSWMDT Mandatory Parameters .............................................................................. 33

*Excerpt: first 8 of 44 pages shown.*
