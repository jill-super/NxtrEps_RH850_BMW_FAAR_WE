---
title: 'ES101A_DiagcMgr_Impl — DiagcMgr_MDD'
description: 'Converted .doc document DiagcMgr_MDD.doc from module ES101A_DiagcMgr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DiagcMgr_MDD.doc` (.doc, 7032 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES101A_DiagcMgr_Impl/doc/DiagcMgr_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shruthi Raghavan, Revision Number: 265, Name of Creating Application: Microsoft Office Word, Total Editing Time: 5d+10:21:00, Create Time/Date: Thu Jan 29 21:19:00 2015, Last Saved Time/Date: Thu Dec 14 20:32:00 2017, Number of Pages: 24, Number of Words: 4486, Number of Characters: 25573, Security: 0; recovered text fragments: 299

## Converted content

## Document outline (extracted text fragments)

- bjbj	@	@
- Module Design Document
- Diagnostic Manager
- VERSION: 1011.0
- DATE:  2614-SEPDEC-2017
- Prepared By:
- Shruthi Raghavan
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Description
- Author
- Version

Initial Version

23-Apr-2015

Added to Design Limitations section

03-Jun-2015

ES101A_DiagcMgr_Design version 2 implementation

11-Mar-2016

ES101A_DiagcMgr_Design version 3 implementation

19-Apr-2016

ES101A_DiagcMgr_Design version 4 implementation

22-Jun-2016

Added DETs to

SetNtcStsCore_Oper

server runnables

26-Sep-2016

Updated to fix anomalies EA4#8118 and EA4#8115

02-Dec-2016

Updated the graphical representation. Added server runnables CnvSnpshtData_*, noted design limitations and design rationales and added local functions

21-Apr-2017

Updated Unit Test considerations as per EA4#9649

29-Jun-2017

Updated Unit Test considerations for new process to handle configuration parameters for PIL testing. Also updated design limitations per latest design baseline.

26-Sep-2017

Removed Static analysis explanation from DiagcMgr PwrDwn function

s rationale because it is no longer applicable. Also removed design limitation that was corrected in the current design version (5.3.0)

14-Dec-2017

Table of Contents

1	Abbrevations And Acronyms

2	References

3	DiagcMgr & High-Level Description

4	Design details of software module

Graphical representation of  Diagcmgr

4.2	Data Flow Diagram

4.2.1	Module level DFD

4.2.2	Sub-Module level DFD

4.3	COMPONENT FLOW DIAGRAM

5	Variable Data Dictionary

5.1	User defined typedef definition/declaration

5.2	Variable definition for enumerated types

5.3	Global Variable definition

6	Constant Data Dictionary

6.1	Program(fixed) Constants

6.1.1	Embedded Constants

6.1.1.1	Local

6.1.1.2	Global

Module specific Lookup Tables Constants

6.1.2

7	Software Module Implementation

7.1	Sub-Module Functions
