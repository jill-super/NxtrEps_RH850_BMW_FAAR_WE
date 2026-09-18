---
title: 'ES300A_SinVltgGenn_Impl — SinVltgGenn_IntegrationManual'
description: 'Converted .doc document SinVltgGenn_IntegrationManual.doc from module ES300A_SinVltgGenn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `SinVltgGenn_IntegrationManual.doc` (.doc, 137 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES300A_SinVltgGenn_Impl/doc/SinVltgGenn_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Windows User, Revision Number: 7, Name of Creating Application: Microsoft Office Word, Total Editing Time: 11:00, Create Time/Date: Sat May  2 19:34:00 2015, Last Saved Time/Date: Mon Jun 15 18:30:00 2015, Number of Pages: 11, Number of Words: 719, Number of Characters: 4104, Security: 0; recovered text fragments: 289

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- Sine Voltage Generation
- VERSION: 1
- DATE: 11-June-2015
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Version
- Description
- Author
- Initial version
- Sankardu Varadapureddi
- 2-May-2015

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

7.3	Non RTE NvM Blocks

7.4	RTE NvM Blocks

8	Compiler Settings

8.1	Preprocessor MACRO

8.2	Optimization Settings

Abbrevations And Acronyms

Abbreviation

Design functional diagram

Module design Document

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

Software Naming Conventions

Process 4.00.00

Software Coding Standards

ES300A_SinVltgGenn_Design

See Synergy sub project version

Dependencies

Module

Required Feature

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

Global Functions(Non RTE) to be provided to Integration Project

SinVltgGennPer1

SinVltgGennPer2

Configuration REQUIREMeNTS

Build Time Config

Modules
