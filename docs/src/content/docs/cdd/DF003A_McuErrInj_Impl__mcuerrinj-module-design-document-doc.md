---
title: 'DF003A_McuErrInj_Impl — McuErrInj Module Design Document'
description: 'Converted .doc document McuErrInj Module Design Document.doc from module DF003A_McuErrInj_Impl.'
sidebar:
  hidden: true
---

> **Source:** `McuErrInj Module Design Document.doc` (.doc, 156 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: DF003A_McuErrInj_Impl/doc/McuErrInj Module Design Document.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Windows User, Template: MDD Template EA4 01.00.01.dotx, Last Saved By: Avinash James, Revision Number: 81, Name of Creating Application: Microsoft Office Word, Total Editing Time: 22:47:00, Last Printed: Wed Dec 17 18:01:00 2014, Create Time/Date: Sun Aug  2 21:20:00 2015, Last Saved Time/Date: Wed Jul 26 19:32:00 2017, Number of Pages: 18, Number of Words: 1670, Number of Characters: 9522, Security: 0; recovered text fragments: 379

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- McuErrInj
- DOCPROPERTY  "Release Date"  \* MERGEFORMAT
- Mar 15, 2017
- Jul 25, 2017
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA

Prepared By:

DOCPROPERTY  "Prepared by Group"  \* MERGEFORMAT

Software G

roup,

Change History

Description

Author

Version

Initial Version

Avinash James

15-Mar-2017

Added the global functions

25-Jul-2017

Table of Contents

1	Introduction

1.1	Purpose

2	McuDiagc & High-Level Description

3	Design details of software module

3.1	Graphical representation of McuDiagc

3.2	Data Flow Diagram

3.2.1	Component level DFD

3.2.2	Function level DFD

4	Constant Data Dictionary

4.1	Program (fixed) Constants

4.1.1	Embedded Constants

5	Software Component Implementation

5.1	Sub-Module Functions

5.1.1	Init: McuErrInjInit1

5.1.1.1	Design Rationale

5.1.1.2	Module Outputs

5.1.2	Per: McuErrInjPer1

5.1.2.1	Design Rationale

5.1.2.2	Store Module Inputs to Local copies

5.1.2.3	(Processing of function)

5.1.2.4	Store Local copy of outputs into Module Outputs

5.1.2.5	Store Local copy of outputs into Module Outputs

5.2	Server Runnable

5.2.1	ClrErrInjReg_Oper

5.2.1.1	Design Rationale

5.2.1.2	Store Module Inputs to Local copies

5.2.1.3	(Processing of function)

5.2.1.4	Store Local copy of outputs into Module Outputs

5.2.1	ReadErrInjReg_Oper

5.2.1	UpdErrInjReg_Oper

5.2.1	StrtErrInjCntr

5.3	Interrupt Functions

5.4	Module Internal (Local) Functions

5.5	GLOBAL Function/Macro Definitions
