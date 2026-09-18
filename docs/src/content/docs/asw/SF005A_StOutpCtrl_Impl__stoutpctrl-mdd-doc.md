---
title: 'SF005A_StOutpCtrl_Impl — StOutpCtrl_MDD'
description: 'Converted .doc document StOutpCtrl_MDD.doc from module SF005A_StOutpCtrl_Impl.'
sidebar:
  hidden: true
---

> **Source:** `StOutpCtrl_MDD.doc` (.doc, 200 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: SF005A_StOutpCtrl_Impl/doc/StOutpCtrl_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Leser, Matt, Revision Number: 7, Name of Creating Application: Microsoft Office Word, Total Editing Time: 11:00, Create Time/Date: Tue Mar 29 22:14:00 2016, Last Saved Time/Date: Mon Dec  5 20:58:00 2016, Number of Pages: 18, Number of Words: 1483, Number of Characters: 8456, Security: 0; recovered text fragments: 434

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- StOutpCtrl
- VERSION: 32.
- DATE:  29-Mar-20165-Dec-2016
- Prepared By:
- Akilan RathakrishnanMatthew Leser
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description
- Author
- Version

Initial Version

Akilan Rathakrishnan

02-June-2015

Implementation of input name change

Basavaraja Ganeshappa

30-June-2016

Updated to fix Anomaly EA4#7767

Matthew Leser

05-Dec-2016

Table of Contents

1	Abbrevations And Acronyms

2	References

3	StOutpCtrl - High-Level Description

4	Design details of software module

4.1	Graphical representation of  StOutpCtrl

4.2	Data Flow Diagram

4.2.1	Module level DFD

4.2.2	Sub-Module level DFD

4.3	COMPONENT FLOW DIAGRAM

5	Variable Data Dictionary

5.1	User defined typedef definition/declaration

5.2	Variable definition for enumerated types

6	Constant Data Dictionary

6.1	Program(fixed) Constants

6.1.1	Embedded Constants

6.1.1.1	Local

6.1.1.2	Global

6.1.2	Module specific Lookup Tables Constants

7	Software Module Implementation

7.1	Sub-Module Functions

7.1.1	Initialization Functions

7.1.1.1	INIT: StOutpCtrlInit1

7.1.1.2	Design Rationale

7.1.1.3	Store Module Inputs to Local copies

7.1.1.4	(Processing of function)

7.1.1.5	Store Local copy of outputs into Module Outputs

7.1.2	PERIODIC FUNCTIONS

7.1.2.1	Per: StOutpCtrlPer1

7.1.2.2	Design Rationale

7.1.2.3	Store Module Inputs to Local copies

7.1.2.4	(Processing of function)

7.1.2.5	Store Local copy of outputs into Module Outputs

7.2	Interrupt Functions

7.3	Serial Communication Functions

7.4	Local Function/Macro Definitions

7.4.1	Local Function #1: RateLimit

7.4.1.1	Description

7.4.1.2	Design Rationale
