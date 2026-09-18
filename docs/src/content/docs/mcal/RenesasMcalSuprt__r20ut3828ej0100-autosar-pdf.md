---
title: 'RenesasMcalSuprt — R20UT3828EJ0100-AUTOSAR'
description: 'Converted PDF document R20UT3828EJ0100-AUTOSAR.pdf from module RenesasMcalSuprt.'
sidebar:
  hidden: true
---

> **Source:** `R20UT3828EJ0100-AUTOSAR.pdf` (PDF, 1940 KB, in-module path `doc/`)
>
> Converted from PDF with text extraction; layout, vector diagrams and scanned figures are not preserved. See the source PDF in the repository for the authoritative content.
>
> pages: 70; title: AUTOSAR MCAL R4.0 User's Manual; author: Renesas Electronics Corporation

## Converted content

### Page 1

Getting Started Document for 
P1x-C MCAL Driver 
 
 
 
 
Version 1.0.2
User's 
Manual 
 
 
 
Target Device: 
RH850/P1x-C 
 
 
 
 
 
 
 
 
All information contained in these materials, including products and product specifications, 
represents information on the product at the time of publication and is subject to change by 
Renesas Electronics Corp. without notice. Please review the latest information published by 
Renesas Electronics Corp. through various means, including the Renesas Electronics Corp. 
website (http://www.renesas.com). 
 
 
 
 
 
 
www.renesas.com Rev.1.00 Feb 2017

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
applications for each

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
<MICRO_VARIANT> P1x-C 
<MICRO_SUB_VARIANT> P1H-C 
AUTOSAR_VERSION 4.0.3 
DEVICE_NAME Example :R7F701372EAFP 
 
 
 
Definitions 
 
 
 
Terminology Description 
.xml XML File. 
.one Project Settings file. 
.arxml AUTOSAR XML File. 
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
Configuration XML File Configuration XML File is in XML format which contains command line options 
and options for input/output file path.

### Page 6

6

### Page 7

7 
Table Of Contents 
 
Chapter 1 Introduction .................................................................... 11 
Chapter 2 ECU Configuration Editor (ECU Spectrum) ................. 13 
2.1. Installation Of ECU Configuration Editor (ECU Spectrum) ............................................... 13 
2.2. ECU Spectrum Input and Output Files ................................................................................. 20 
Chapter 3 Configuration Using ECU Configuration Editor (ECU 
Spectrum) ......................................................................................... 21 
3.1. Creating New Project ............................................................................................................. 21 
3.2. Configuration .......................................................................................................................... 22 
3.2.1. Parameter Configuration .............................................................................................. 24 
3.2.2. Distinguish Between Containers .................................................................................. 24 
3.2.3. Save Project................................................................................................................. 25 
3.2.4. Validation ..................................................................................................................... 25 
3.3. Generate ECU Configuration Description ........................................................................... 26 
Chapter 4 Generation Tool .............................................................. 29 
4.1. ECU Configuration Description File .............................................................................................. 29 
4.2. Velocity template files 

### Page 8

8 
5.4. Makefile Description .............................................................................................................. 45 
5.4.1. App_<Msn>_<variant>_Sample.mak .......................................................................... 46 
5.5. Integrating The <MSN> Driver Component With Other Components ............................ 51 
5.6. Building The <MSN> Driver Component ............................................................................. 52 
5.6.1. Targets Supported By The Sample Base Makefile ..................................................... 54 
Chapter 6 Support For Different Interrupt Categories .................. 57 
Chapter 7 GNU MAKE Environment ............................................... 59 
7.1. Build Process With GNUMAKE ............................................................................................. 59 
7.2. Build Process Without GNUMAKE ....................................................................................... 59 
Chapter 8 Load Binaries ................................................................. 63 
Chapter 9 Appendix......................................................................... 65

*Excerpt: first 8 of 70 pages shown.*
