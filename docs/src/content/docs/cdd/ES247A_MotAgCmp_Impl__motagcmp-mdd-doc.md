---
title: 'ES247A_MotAgCmp_Impl — MotAgCmp_MDD'
description: 'Converted .doc document MotAgCmp_MDD.doc from module ES247A_MotAgCmp_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAgCmp_MDD.doc` (.doc, 180 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES247A_MotAgCmp_Impl/doc/MotAgCmp_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shawn Penning, Revision Number: 5, Name of Creating Application: Microsoft Office Word, Total Editing Time: 51:00, Create Time/Date: Fri Sep  1 17:14:00 2017, Last Saved Time/Date: Thu Dec  7 15:47:00 2017, Number of Pages: 15, Number of Words: 1227, Number of Characters: 6996, Security: 0; recovered text fragments: 407

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- MotAgCmp
- VERSION: 43.0
- DATE:  16-Nov-201609-Sep-2017
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA
- Prepared By:

TATA ELXSIShawn Penning

CHENNAI, INDIASaginaw, MI

Revision History

Sl. No.

Description

Author

Version

Initial Version

02-JUN-2015

Updated per design rev. 1.5.0

Rijvi

13-OCT-2016

Updated per design rev. 1.7.0

16-NOV-2016

Added to Unit Test Considerations

09-SEP-2017

Table of Contents

1	Abbrevations And Acronyms

2	References

3	motagcmp & High-Level Description

4	Design details of software module

4.1	Graphical representation of motagcmp

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

7.2.1.1	MotAgCmpInit1

7.2.1.2	Design Rationale

7.3	PERIODIC FUNCTIONS

7.3.1	Per: Motagcmpper1

7.3.1.1	Design Rationale

7.3.1.2	Store Module Inputs to Local copies

7.3.1.3	(Processing of function)

7.3.1.4	Store Local copy of outputs into Module Outputs

7.3.2	Per: Motagcmpper2

7.3.2.1	Design Rationale
