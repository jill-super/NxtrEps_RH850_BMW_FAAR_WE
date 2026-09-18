---
title: 'AR202A_MicroCtrlrSuprt_Impl — MicroCtrlrSuprt Integration Manual'
description: 'Converted .doc document MicroCtrlrSuprt Integration Manual.doc from module AR202A_MicroCtrlrSuprt_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MicroCtrlrSuprt Integration Manual.doc` (.doc, 154 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: AR202A_MicroCtrlrSuprt_Impl/doc/MicroCtrlrSuprt Integration Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Lucas Wendling, Revision Number: 18, Name of Creating Application: Microsoft Office Word, Total Editing Time: 49:00, Create Time/Date: Mon Jul 10 01:42:00 2017, Last Saved Time/Date: Wed Jul 19 12:05:00 2017, Number of Pages: 13, Number of Words: 1179, Number of Characters: 6723, Security: 0; recovered text fragments: 320

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- MicroCtrlrSuprt
- VERSION: 1
- DATE: 07/19/17
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

07/19/17

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

This component is dependant on the v800_ghs.h compiler header file for definition of some compiler intrinsic functions.

Module

Required Feature

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

Global Functions(Non RTE) to be provided to Integration Project

This component provides the following inline functions in NxtrMcuSuprtLib.h for use as needed in components and integration project.  Note that the exact API for usage can be found in the header file.

For P1M devices:

Function Name

WrProtdRegPortJ_u32

Protected Register write sequence for 32bit PortJ peripheral registers
