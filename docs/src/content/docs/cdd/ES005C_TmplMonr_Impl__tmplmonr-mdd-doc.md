---
title: 'ES005C_TmplMonr_Impl — TmplMonr_MDD'
description: 'Converted .doc document TmplMonr_MDD.doc from module ES005C_TmplMonr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `TmplMonr_MDD.doc` (.doc, 198 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES005C_TmplMonr_Impl/doc/TmplMonr_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Windows User, Template: MDD Template EA4 01.00.01.dotx, Last Saved By: Krishna Anne, Revision Number: 29, Name of Creating Application: Microsoft Office Word, Total Editing Time: 06:13:00, Last Printed: Wed Dec 17 18:01:00 2014, Create Time/Date: Sun Aug  2 21:20:00 2015, Last Saved Time/Date: Mon Mar 27 16:11:00 2017, Number of Pages: 20, Number of Words: 2028, Number of Characters: 11565, Security: 0; recovered text fragments: 423

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- DOCPROPERTY  "Document Version"  \* MERGEFORMAT
- Temporal Monitor Function
- Mar 24, 2017
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA
- Prepared By:

DOCPROPERTY  "Prepared by Group"  \* MERGEFORMAT

Software G

roup,

Change History

Description

Author

Version

Initial Version

Krishna Anne

24-Mar-2017

Removed limitations from previous version

27-Mar-2017

Table of Contents

1	Introduction

1.1	Purpose

2	TmplMonr & High-Level Description

3	Design details of software module

3.1	Graphical representation of TmplMonr

3.2	Data Flow Diagram

3.2.1	Component level DFD

3.2.2	Function level DFD

4	Constant Data Dictionary

4.1	Program (fixed) Constants

4.1.1	Embedded Constants

5	Software Component Implementation

5.1	Sub-Module Functions

5.1.1	Init: TmplMonrInit1

5.1.1.1	Design Rationale

5.1.1.2	Module Outputs

5.1.2	Per: TmplMonrPer1

5.1.2.1	Design Rationale

5.1.2.2	Store Module Inputs to Local copies

5.1.2.3	(Processing of function)

5.1.2.4	Store Local copy of outputs into Module Outputs

5.1.3	Per: TmplMonrPer2

5.1.3.1	Design Rationale

5.1.3.2	Store Module Inputs to Local copies

5.1.3.3	(Processing of function)

5.1.3.4	Store Local copy of outputs into Module Outputs

5.1.4	Per: TmplMonrPer3

5.1.4.1	Design Rationale

5.1.4.2	Store Module Inputs to Local copies

5.1.4.3	(Processing of function)

5.1.4.4	Store Local copy of outputs into Module Outputs

5.2	Server Runables

5.3	Interrupt Functions

5.4	Module Internal (Local) Functions

5.4.1	Local Function #1
