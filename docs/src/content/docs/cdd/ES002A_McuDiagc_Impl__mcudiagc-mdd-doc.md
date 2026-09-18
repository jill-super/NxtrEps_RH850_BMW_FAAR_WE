---
title: 'ES002A_McuDiagc_Impl — McuDiagc_MDD'
description: 'Converted .doc document McuDiagc_MDD.doc from module ES002A_McuDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `McuDiagc_MDD.doc` (.doc, 178 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES002A_McuDiagc_Impl/doc/McuDiagc_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Windows User, Template: MDD Template EA4 01.00.01.dotx, Last Saved By: Brendon Binder, Revision Number: 3, Name of Creating Application: Microsoft Office Word, Last Printed: Wed Dec 17 18:01:00 2014, Create Time/Date: Fri Oct 27 12:22:00 2017, Last Saved Time/Date: Fri Oct 27 12:25:00 2017, Number of Pages: 18, Number of Words: 1324, Number of Characters: 7550, Security: 0; recovered text fragments: 460

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- McuDiagc
- DOCPROPERTY  "Release Date"  \* MERGEFORMAT
- 27-Oct-Sep 28, 2016
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA
- Prepared By:

Brendon Binder

DOCPROPERTY  "Prepared by Group"  \* MERGEFORMAT

Software G

roup,

Change History

Description

Author

Version

Initial Version

Selva Sengottaiyan

29-Mar-2016

Updated for the 2Millisecond to MotorControl Diagnostic and changed NTC logic

Avinash James

22-Jun-2016

Optimized the diagniostics and removed periodic 3

28-Sep-2016

Added SysSt input and updated DaVinci model

27-Oct-2017

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

5.1.1	Init: McuDiagcInit1

5.1.1.1	Design Rationale

5.1.1.2	Module Outputs

5.1.2	Per: McuDiagcPer1

5.1.2.1	Design Rationale

5.1.2.2	Store Module Inputs to Local copies

5.1.2.3	(Processing of function)

5.1.2.4	Store Local copy of outputs into Module Outputs

5.1.3	Per: McuDiagcPer2

5.1.3.1	Design Rationale

5.1.3.2	Store Module Inputs to Local copies

5.1.3.3	(Processing of function)

5.1.3.4	Store Local copy of outputs into Module Outputs

5.2	Server Runnable

5.3	Interrupt Functions

5.4	Module Internal (Local) Functions
