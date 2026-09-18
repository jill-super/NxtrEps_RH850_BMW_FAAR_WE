---
title: 'RenesasMcalSuprt — R20UT3753EJ0101-AUTOSAR'
description: 'Converted PDF document R20UT3753EJ0101-AUTOSAR.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3753EJ0101-AUTOSAR.pdf` (PDF, 793 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 50; title: AUTOSAR MCAL R4.0 User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

Getting Started Document for 
X1x MCAL Driver 
 
 
 
 
Version.1.0.8
User’s 
Manual 
 
 
 
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
applications fo

### Page 4

4

### Page 5

5 
Abbreviations and Acronyms 
 
 
 
Abbreviation / Acronym Description 
ARXML/arxml AUTOSAR xml 
AUTOSAR Automotive Open System Architecture 
BSWMDT Basic Software Module Description Template 
<MSN> Module Short Name 
ECU Electronic Control Unit 
GUI Graphical User Interface 
MB Mega Bytes 
MHz Mega Hertz 
RAM Random Access Memory 
xml/XML eXtensible Markup Language 
<MICRO_VARIANT> F1x, R1x, P1x, E1x etc. 
<MICRO_SUB_VARIANT> F1L,F1M,F1H, R1L, P1L,P1M, E1L, E1MS etc. 
AUTOSAR_VERSION 3.2.2 or 4.0.3 
DEVICE_NAME Example :701205EAFP 
RUCG Renesas Unified Code Generator 
.DLL Dynamic Linking Library 
 
 
 
Definitions 
 
 
 
Terminology Description 
.xml XML File. 
.arxml AUTOSAR XML File. 
.trxml Translation XML File. 
ECU Configuration 
Parameter Definition File 
The ECU Configuration Parameter Definition is of type XML, which contains the 
definition for AUTOSAR software components i.e. definitions for Modules, 
Containers and Parameters. The format of the XML File will be compliant with 
AUTOSAR ECU specification standards. 
ECU Configuration 
Description File 
The ECU Configuration Description file in XML format, which contains the 
configured values for Parameters, Containers and Modules. ECU Configuration 
Description XML File format will be compliant with the AUTOSAR ECU 
specification standards. 
BSWMDT File The BSWMDT File in XML format, which is the template for the Basic Software 
Module Description. BSWMDT File format will be compliant with the AUTOSAR 
BSWMDT specification standards. 
Translation XML File Translation XML File is in XML format, which contains translation and 
device specific header file path. 
Configuration XML File Configuration XML File is in XML format, which contains command line 
options and options for input/output file path.

### Page 6

6

### Page 7

7 
Table of Contents 
 
Chapter 1 Introduction ..................................................................... 11 
Chapter 2 Generation Tool ............................................................... 13 
2.1. Translation XML File ................................................................................................................ 13 
2.1.1. Translation Header File ................................................................................................ 14 
2.1.2. Device Specific Header File .......................................................................................... 14 
2.2. Configuration XML File ........................................................................................................... 14 
2.3. Usage ........................................................................................................................................ 15 
2.4. Sample Usage .......................................................................................................................... 16 
2.5. Tool Installation Requirements .............................................................................................. 18 
2.5.1. Hardware Requirements ............................................................................................... 18 
2.5.2. Software Requirements ................................................................................................. 18 
2.5.3. Limitations ..................................................................................................................... 18 
2.6. Tool Installation ....................................................................................................................... 18 
2.6.1. Pre Requisite .......................................

### Page 8

8 
Chapter 6 Load Binaries .................................................................. 43 
Chapter 7 Appendix.......................................................................... 45 
7.1. Translation XML File ................................................................................................................ 45 
7.2. Configuration XML File ................................................................................................................. 45

*Excerpt: first 8 of 50 pages shown.*
