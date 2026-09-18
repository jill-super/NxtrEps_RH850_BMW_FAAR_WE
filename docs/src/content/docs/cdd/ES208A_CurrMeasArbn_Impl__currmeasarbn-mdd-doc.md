---
title: 'ES208A_CurrMeasArbn_Impl — CurrMeasArbn_MDD'
description: 'Converted .doc document CurrMeasArbn_MDD.doc from module ES208A_CurrMeasArbn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CurrMeasArbn_MDD.doc` (.doc, 160 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES208A_CurrMeasArbn_Impl/doc/CurrMeasArbn_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Sengottaiyan, Selva, Template: MDD Template EA4 01.00.01.dotx, Last Saved By: Sengottaiyan, Selva, Revision Number: 10, Name of Creating Application: Microsoft Office Word, Total Editing Time: 23:00, Last Printed: Wed Dec 17 17:01:00 2014, Create Time/Date: Thu Sep 17 17:21:00 2015, Last Saved Time/Date: Sun Mar 20 20:42:00 2016, Number of Pages: 17, Number of Words: 1461, Number of Characters: 8330, Security: 0; recovered text fragments: 389

## Converted content

## Document outline (extracted text fragments)

- bjbjupup
- Module Design Document
- Current Measurement Arbitration
- DOCPROPERTY  "Release Date"  \* MERGEFORMAT
- Sep 18, 2015
- Mar 18, 201
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT

Saginaw, MI, USA

Prepared By:

DOCPROPERTY  "Prepared by Group"  \* MERGEFORMAT

Change History

Description

Author

Version

Initial Version

Selva

14- Apr-2015

Updated for Anomoly EA4#1589 . Combined MDD for both sources files

17 -Sep 2015

Updated for Anomoly EA4#2989

18 -Mar 2016

< Remove change history for template and enter change history for MDD document>

Table of Contents

1	Introduction

1.1	Purpose

1.2	Scope

2	Current Measurement Arbitration & High-Level Description

3	Design details of software module

3.1	Graphical representation of Current Measurement Arbitration

3.2	Data Flow Diagram

3.2.1	Component level DFD

3.2.2	Function level DFD

4	Constant Data Dictionary

4.1	Program (fixed) Constants

4.1.1	Embedded Constants

5	Software Component Implementation

5.1	Sub-Module Functions

5.1.1	Init: CurrMeasArbnInit1

5.1.1.1	Design Rationale

5.1.1.2	Module Outputs

5.1.1.3	Per:

5.1.1.4	CurrMeasARBNPer1

5.1.1.5	Design Rationale

5.1.1.6	Store Module Inputs to Local copies

5.1.1.7	(Processing of function)

5.1.1.8	Store Local copy of outputs into Module Outputs

5.2	Server Runables

5.3	Interrupt Functions

5.4	Module Internal (Local) Functions

5.5	Local Function/Macro Definitions

5.5.1	Local Function #1 SigAvlCheck

5.5.1.1	Description

5.5.2	Local Function #2 ParkTransformation

5.5.2.1	Description

5.6	GLOBAL Function/Macro Definitions
