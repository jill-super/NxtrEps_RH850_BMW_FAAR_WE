---
title: 'CM107A_GuardCfgAndDiagc_Impl — GuardCfgAndDiagc Integration Manual'
description: 'Converted .doc document GuardCfgAndDiagc Integration Manual.doc from module CM107A_GuardCfgAndDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `GuardCfgAndDiagc Integration Manual.doc` (.doc, 150 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM107A_GuardCfgAndDiagc_Impl/doc/GuardCfgAndDiagc Integration Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Avinash James, Revision Number: 24, Name of Creating Application: Microsoft Office Word, Total Editing Time: 02:58:00, Create Time/Date: Thu Jul 17 15:54:00 2014, Last Saved Time/Date: Tue Mar 21 13:37:00 2017, Number of Pages: 12, Number of Words: 803, Number of Characters: 4578, Security: 0; recovered text fragments: 305

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- GuardCfgAndDiagc
- VERSION: 12
- DATE: 0203/1621/1617
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

Avinash James

02/16/16

Updated to include build paaramters for micro diag special build

03/21/17

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

7.3	NvM Blocks

8	Compiler Settings

8.1	Preprocessor MACRO

8.2	Optimization Settings

9	Appendix

Abbrevations And Acronyms

Abbreviation

Design functional diagram

Module design Document

Functional Design Document

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

CM107A GuardCfgAndDiagc

See Synergy subproject version

Software Naming Conventions

Process 04.02.00

Software Coding Standards

Dependencies

Module
