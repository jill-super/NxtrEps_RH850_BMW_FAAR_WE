---
title: 'ES259B_BattVltgCorrln_Impl — BattVltgCorrln_MDD'
description: 'Converted .doc document BattVltgCorrln_MDD.doc from module ES259B_BattVltgCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BattVltgCorrln_MDD.doc` (.doc, 230 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES259B_BattVltgCorrln_Impl/doc/BattVltgCorrln_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: Module Design Document, Author: Nexteer Employee, Template: MDD Template EA4 01.00.00.dotx, Last Saved By: Brionna Spencer, Revision Number: 27, Name of Creating Application: Microsoft Office Word, Total Editing Time: 57:00, Last Printed: Wed Dec 17 18:01:00 2014, Create Time/Date: Tue May 23 19:14:00 2017, Last Saved Time/Date: Tue Jun 27 19:40:00 2017, Number of Pages: 15, Number of Words: 1176, Number of Characters: 6706, Security: 0; recovered text fragments: 587

## Converted content

## Document outline (extracted text fragments)

- Module Design Document
- BattVltgCorrln
- DOCPROPERTY  "Release Date"  \* MERGEFORMAT
- June 7, 2016
- 27-Jun-2017
- Prepared For:
- DOCPROPERTY  "Prepared for Group"  \* MERGEFORMAT
- Software Engineering
- DOCPROPERTY  Company  \* MERGEFORMAT
- Nexteer Automotive
- DOCPROPERTY  Location  \* MERGEFORMAT
- Saginaw, MI, USA

Prepared By:

Nick SaxtonBrionna Spencer,

Change History

Description

Author

Version

Initial Version

N. Saxton

7-Jun-2016

Updated the graphical representation, added design rationale for BattVltgCorrlnPer1, and updated the documentation for modified local functions (i.e. DetInstCorrln, DetIdptSig, and DetCorrlnSts).

B. Spencer

Table of Contents

1	BattVltgCorrln & High-Level Description

2	Design details of software module

2.1	Graphical representation of BattVltgCorrln

2.2	Data Flow Diagram

2.2.1	Component level DFD

2.2.2	Function level DFD

3	Constant Data Dictionary

3.1	Program (fixed) Constants

3.1.1	Embedded Constants

4	Software Component Implementation

4.1.1	Sub-Module Functions

4.1.2	Interrupt Service Routines

4.1.3	Server Runnable Functions

4.1.4	Module Internal (Local) Functions

4.1.5	Transition Functions

5	Known Limitations with Design

6	UNIT TEST CONSIDERATION

Appendix A	Abbreviations and Acronyms

Appendix B	Glossary

Appendix C	References

BattVltgCorrln & High-Level Description

Refer FDD

Design details of software module

Graphical representation of BattVltgCorrln

Data Flow Diagram

Component level DFD

Function level DFD

Constant Data Dictionary

Program (fixed) Constants

Embedded Constants

Local Constants

Constant Name

Resolution

Units

Value

BATTVLTGIDPTSIGMIN_CNT_U08
