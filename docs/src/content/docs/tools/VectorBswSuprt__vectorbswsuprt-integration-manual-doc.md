---
title: 'VectorBswSuprt — VectorBswSuprt Integration Manual'
description: 'Converted .doc document VectorBswSuprt Integration Manual.doc from module VectorBswSuprt.'
sidebar:
  hidden: true
---

> **Source:** `VectorBswSuprt Integration Manual.doc` (.doc, 131 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: VectorBswSuprt/doc/VectorBswSuprt Integration Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Lucas Wendling, Revision Number: 9, Name of Creating Application: Microsoft Office Word, Total Editing Time: 02:29:00, Create Time/Date: Wed Feb  1 15:27:00 2017, Last Saved Time/Date: Thu Feb  2 21:34:00 2017, Number of Pages: 12, Number of Words: 828, Number of Characters: 4720, Security: 0; recovered text fragments: 273

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- VectorBswSuprt
- VERSION: 1
- DATE: 02/01/17
- Prepared By:
- Software Group,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description

Author

Version

Initial version

Lucas Wendling

02/01/17

Table of Contents

1	Abbrevations And Acronyms

2	References

3	Dependencies

3.1	SWCs

3.2	Global Functions(Non RTE) to be provided to Integration Project

4	Configuration REQUIREMeNTS

4.1	Build Time Config

4.2	Configuration Files to be provided by Integration Project

4.3	Da Vinci Parameter Configuration Changes

4.4	DaVinci Interrupt Configuration Changes

4.5	Manual Configuration Changes

5	Integration  DATAFLOW REQUIREMENTS

5.1	Required Global Data Inputs

5.2	Required Global Data Outputs

5.3	Specific Include Path present

6	Runnable Scheduling

7	Memory Map REQUIREMENTS

7.1	Mapping

7.2	Usage

7.3	Non  RTE NvM Blocks

7.4	RTE NvM Blocks

8	Compiler Settings

8.1	Preprocessor MACRO

8.2	Optimization Settings

9	Appendix

Abbrevations And Acronyms

Abbreviation

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

Dependencies

Module

Required Feature

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

Global Functions(Non RTE) to be provided to Integration Project

Configuration REQUIREMeNTS

s Vector SIP delivery) by using the appropriate Green Hills .gpj subproject as will as pointing the include search path to the appropriate subdirectory of this component.

tools/template/

folder of this component.  For details on how to adapt, third party documentation found in this component can be referenced as needed.

Build Time Config

Modules
