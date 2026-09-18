---
title: 'ES008A_PwrSply_Impl — PwrSply_MDD'
description: 'Converted .doc document PwrSply_MDD.doc from module ES008A_PwrSply_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PwrSply_MDD.doc` (.doc, 132 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES008A_PwrSply_Impl/doc/PwrSply_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Windows User, Template: MDD Template EA4 01.00.01 (2).dotx, Last Saved By: Krishna Anne, Revision Number: 3, Name of Creating Application: Microsoft Office Word, Last Printed: Wed Dec 17 18:01:00 2014, Create Time/Date: Mon Mar 20 18:54:00 2017, Last Saved Time/Date: Mon Mar 20 18:54:00 2017, Number of Pages: 15, Number of Words: 991, Number of Characters: 5650, Security: 0; recovered text fragments: 360

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- PwrSply
- MarApril 204, 20176
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA
- Prepared By:
- Software Group,

Change History

Description

Author

Version

Initial Version

Rijvi Ahmed

15-Sep-2015

Updated per design rev. 1.4.0

04-April-2016

Updated per design rev. 1.7.0

Krishna Anne

20-Mar-17

Table of Contents

1	Introduction

2	PwrSply & High-Level Description

3	Design details of software module

3.1	Graphical representation of PwrSply

3.2	Data Flow Diagram

3.2.1	Component level DFD

3.2.2	Function level DFD

4	Constant Data Dictionary

4.1	Program (fixed) Constants

4.1.1	Embedded Constants

5	Software Component Implementation

5.1	Sub-Module Functions

5.1.1	Init: PwrSplyInit1

5.1.1.1	Design Rationale

5.1.1.2	(Processing of function)

5.1.2	Per:   PwrSplyPer1

5.1.2.1	Design Rationale

5.1.2.2	Store Module Inputs to Local copies

5.1.2.3	(Processing of function)

5.1.2.4	Store Local copy of outputs into Module Outputs

5.2	Server Runnable

5.3	Interrupt Functions

5.4	Module Internal (Local) Functions

5.5	GLOBAL Function/Macro Definitions

6	Known Limitations with Design

7	UNIT TEST CONSIDERATION

Appendix A	Abbreviations and Acronyms

Appendix B	Glossary

Appendix C	References

Introduction

PwrSply & High-Level Description

Design details of software module

<The Data Flow Diagrams should be created in the absence of this representation with the FDD.>

Graphical representation of PwrSply

Data Flow Diagram
