---
title: 'ES311A_GateDrv0Ctrl_Impl — GateDrv0Ctrl_IntegrationManual'
description: 'Converted .doc document GateDrv0Ctrl_IntegrationManual.doc from module ES311A_GateDrv0Ctrl_Impl.'
sidebar:
  hidden: true
---

> **Source:** `GateDrv0Ctrl_IntegrationManual.doc` (.doc, 143 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES311A_GateDrv0Ctrl_Impl/doc/GateDrv0Ctrl_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shruthi Raghavan, Revision Number: 14, Name of Creating Application: Microsoft Office Word, Total Editing Time: 01:04:00, Create Time/Date: Fri Jul  8 17:37:00 2016, Last Saved Time/Date: Tue Sep 12 16:08:00 2017, Number of Pages: 11, Number of Words: 776, Number of Characters: 4427, Security: 0; recovered text fragments: 302

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- Gate Drive 0 Control
- VERSION: 23
- DATE: 1511-MarSep-2017
- Prepared By:
- Shruthi Raghavan,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Version
- Description

Author

Initial version

Rijvi Ahmed

08-July-2016

Updated for SPI MCAL update in FDD v2.2.0

Shruthi Raghavan

15-Mar-2017

Details of new config parameter added.

11-Sep-2017

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

Process 04.024.012

Software Coding Standards

ES311A GateDrv0Ctrl

See synergy sub project version

Dependencies
