---
title: 'RenesasMcalSuprt — R20UT3753EJ0100-AUTOSAR'
description: 'Converted PDF document R20UT3753EJ0100-AUTOSAR.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3753EJ0100-AUTOSAR.pdf` (PDF, 721 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 50; title: AUTOSAR MCAL R4.0 User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

Getting Started Document for 
X1x MCAL Driver 
 
 
 
 
Version.1.0.7
User’s 
Manual 
 
 
 
Target Device: 
RH850/P1x 
 
 
 
 
 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
 
 
 
www.renesas.com Rev.1.00 Jun 2016

### Page 2

2

### Page 3

3 
Notice 
1. All information included in this document is current as of the date this document is issued. Such information, however, is 
subject to change without any prior notice. Before purchasing or using any Renesas Electronics products listed herein, please 
confirm the latest product information with a Renesas Electronics sales office. Also, please pay regular and careful attention to 
additional and different information to be disclosed by Renesas Electronics such as that disclosed through our website. 
2. Renesas Electronics does not assume any liability for infringement of patents, copyrights, or other intellectual property rights 
of third parties by or arising from the use of Renesas Electronics products or technical information described in this document. 
No license, express, implied or otherwise, is granted hereby under any patents, copyrights or other intellectual property rights 
of Renesas Electronics or others. 
3. You should not alter, modify, copy, or otherwise misappropriate any Renesas Electronics product, whether in whole or in part. 
4. Descriptions of circuits, software and other related information in this document are provided only to illustrate the operation of 
semiconductor products and application examples. You are fully responsible for the incorporation of these circuits, software, 
and information in the design of your equipment. Renesas Electronics assumes no responsibility for any losses incurred by 
you or third parties arising from the use of these circuits, software, or information. 
5. When exporting the products or technology described in this document, you should comply with the applicable export control 
laws and regulations and follow the procedures required by such laws and regulations. You should not use Renesas 
Electronics

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
Translation XML File Translation XML File is in XML format which contains translation and device 
specific header file path. 
Configuration XML File Configuration XML File is in XML format which contains command line options 
and options for input/output file path.

### Page 6

6

### Page 7

7 
Table Of Contents 
 
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
