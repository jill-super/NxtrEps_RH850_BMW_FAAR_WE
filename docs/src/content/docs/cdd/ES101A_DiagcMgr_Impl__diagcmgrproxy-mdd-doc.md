---
title: 'ES101A_DiagcMgr_Impl — DiagcMgrProxy_MDD'
description: 'Converted .doc document DiagcMgrProxy_MDD.doc from module ES101A_DiagcMgr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DiagcMgrProxy_MDD.doc` (.doc, 1674 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES101A_DiagcMgr_Impl/doc/DiagcMgrProxy_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shruthi Raghavan, Revision Number: 28, Name of Creating Application: Microsoft Office Word, Total Editing Time: 42:00, Create Time/Date: Fri Dec  2 15:06:00 2016, Last Saved Time/Date: Thu Jun 29 18:56:00 2017, Number of Pages: 19, Number of Words: 1735, Number of Characters: 9891, Security: 0; recovered text fragments: 469

## Converted content

## Document outline (extracted text fragments)

- wAdj-
- Module Design Document
- Diagnostic Manager Proxy
- VERSION: 45.0
- DATE:  2129-JUNAPR-2017
- Prepared By:
- Shruthi Raghavan
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description
- Author

Version

ES101A_DiagcMgr_Design version 2 implementation

11-Mar-2016

ES101A_DiagcMgr_Design version 4 implementation

22-Jun-2016

Added new DET in Init1

02-Dec-2016

Added new runnable SetNtcStsAndSnpshtData.

21-Apr-2017

Added unit test considerations per EA4#9649

29-Jun-2017

Table of Contents

1	Abbrevations And Acronyms

2	References

3	DiagcMgrPROXYAPPLX & High-Level Description

4	Design details of software module

4.1	Graphical representation of  DiagcmgrPRoxyApplX

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

7.1.1.1	INIT: DiagcMgrPROXYAPPLXInit1

7.1.1.2	Design Rationale

7.1.1.3	Store Module Inputs to Local copies

7.1.1.4	(Processing of function)

7.1.1.5	Store Local copy of outputs into Module Outputs

7.1.2	PERIODIC FUNCTIONS

7.1.2.1	Per: diagcmgrPROXYAPPLXPer1

7.1.2.2	Design Rationale

7.1.2.3	Store Module Inputs to Local copies

7.1.2.4	(Processing of function)

7.1.2.5	Store Local copy of outputs into Module Outputs

7.1.3	Interrupt Functions

7.1.4	Server Runnable Functions

7.1.4.1	GetDiagcDataApplX_Oper

7.1.4.2	GetNtcActvX_Oper
