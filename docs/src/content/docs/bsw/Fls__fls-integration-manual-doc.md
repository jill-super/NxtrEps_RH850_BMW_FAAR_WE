---
title: 'Fls — Fls Integration Manual'
description: 'Converted .doc document Fls Integration Manual.doc from module Fls.'
sidebar:
  hidden: true
---

> **Source:** `Fls Integration Manual.doc` (.doc, 256 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: Fls/doc/Fls Integration Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Lucas Wendling, Revision Number: 26, Name of Creating Application: Microsoft Office Word, Total Editing Time: 02:53:00, Create Time/Date: Thu Jul 17 15:54:00 2014, Last Saved Time/Date: Mon May  8 13:49:00 2017, Number of Pages: 13, Number of Words: 1286, Number of Characters: 7335, Security: 0; recovered text fragments: 204

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- VERSION: 3
- DATE: 05/08/2017
- Prepared By:
- Software Group,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description
- Author

Version

Initial version

Rijvi Ahmed

03/03/17

Updated for callout function mapping

05/05/2017

Updates for compiler settings

Lucas Wendling

05/08/2017

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

API usage and scheduling of BSW components expected to be captured at a project architectural level and is beyond the scope of this document.  Third party documentation can be referenced as needed.

Configuration REQUIREMeNTS
