---
title: 'ES250B_BattVltg_Impl — BattVltg_IntegrationManual'
description: 'Converted .doc document BattVltg_IntegrationManual.doc from module ES250B_BattVltg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BattVltg_IntegrationManual.doc` (.doc, 136 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES250B_BattVltg_Impl/doc/BattVltg_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Nexteer Employee, Revision Number: 26, Name of Creating Application: Microsoft Office Word, Total Editing Time: 26:00, Create Time/Date: Thu Jul 17 15:54:00 2014, Last Saved Time/Date: Wed May 18 13:33:00 2016, Number of Pages: 12, Number of Words: 671, Number of Characters: 3828, Security: 0; recovered text fragments: 290

## Converted content

## Document outline (extracted text fragments)

- bjbjupup
- Integration Manual
- BattVltg
- VERSION: 1.0
- DATE: 18-MAY-2016
- Prepared By:
- Nick Saxton,
- Nexteer Automotive,
- Saginaw, MI, USA
- Revision History
- Description
- Author

Version

Initial version

N. Saxton

18-May-2016

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

Design functional diagram

Module design Document

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

EA4 Software Naming Conventions.doc

01.00.00

Software Design and Coding Standards.doc

ES250B_BattVltg_Design

See Synergy subproject version

Dependencies

Module

Required Feature

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

Global Functions(Non RTE) to be provided to Integration Project
