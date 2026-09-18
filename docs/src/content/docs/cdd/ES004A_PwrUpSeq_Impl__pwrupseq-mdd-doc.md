---
title: 'ES004A_PwrUpSeq_Impl — PwrUpSeq_MDD'
description: 'Converted .doc document PwrUpSeq_MDD.doc from module ES004A_PwrUpSeq_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PwrUpSeq_MDD.doc` (.doc, 198 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES004A_PwrUpSeq_Impl/doc/PwrUpSeq_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Krishna Anne, Revision Number: 41, Name of Creating Application: Microsoft Office Word, Total Editing Time: 03:46:00, Create Time/Date: Thu Jan 29 21:19:00 2015, Last Saved Time/Date: Mon Nov 13 22:28:00 2017, Number of Pages: 17, Number of Words: 1141, Number of Characters: 6510, Security: 0; recovered text fragments: 458

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- Power Up Sequence
- VERSION: 54.0
- DATE: 0704-NOVJAN-2017
- Prepared By:
- TATA ELXSI,
- TRIVANDRUM, INDIA
- Software Group,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History

Sl. No.

Description

Author

Version

Initial Version

Rijvi Ahmed

11-Apr-2015

Updated for FDD ver 1.2.0

Sankardu Varadapureddi

13-Jan-2016

Updated for FDD ver 1.4.0

15-July-2016

Updated for FDD ver 1.5.0

Avinash James

04-Jan-2017

Updated for FDD ver 2.0.0

07-Nov-2017

Table of Contents

1	Abbrevations And Acronyms

2	References

3	MDD pwrupseq & High-Level Description

4	Design details of software module

4.1	Graphical representation of pwrupseq

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

7.2	Initialization Functions

7.2.1	PwrUpSeqInit1

7.2.1.1	Design Rationale

7.2.1.2	Module Outputs

7.3	PERIODIC FUNCTIONS

7.3.1	Per: PwrUpSeqPer1

7.3.1.1	Design Rationale

7.3.1.2	Store Module Inputs to Local copies

7.3.1.3	(Processing of function)

7.3.1.4	Store Local copy of outputs into Module Outputs
