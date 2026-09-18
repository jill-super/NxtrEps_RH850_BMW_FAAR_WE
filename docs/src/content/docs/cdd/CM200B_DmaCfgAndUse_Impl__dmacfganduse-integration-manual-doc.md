---
title: 'CM200B_DmaCfgAndUse_Impl — DmaCfgAndUse_Integration_Manual'
description: 'Converted .doc document DmaCfgAndUse_Integration_Manual.doc from module CM200B_DmaCfgAndUse_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DmaCfgAndUse_Integration_Manual.doc` (.doc, 141 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM200B_DmaCfgAndUse_Impl/doc/DmaCfgAndUse_Integration_Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Byrski, Krzysztof, Revision Number: 25, Name of Creating Application: Microsoft Office Word, Total Editing Time: 47:00, Create Time/Date: Thu Jul 17 10:54:00 2014, Last Saved Time/Date: Mon Dec  4 13:21:00 2017, Number of Pages: 12, Number of Words: 830, Number of Characters: 4733, Security: 0; recovered text fragments: 310

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- DmaCfgAndUse
- VERSION: 12.0
- DATE: 2704-MayDec-20176
- Prepared By:
- Avinash James
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Description
- Author
- Version
- Initial version

27-May-2016

Updated as per Design 3.0.0

Krzysztof Byrski

04-Dec-2017

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

<ADD  more to the table if applicable>

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

CM200B DmaCfgAndUse

See Synergy subproject version

Software Naming Conventions

Process 04.02.01

Software Coding Standards

Dependencies

Module

Required Feature

MotCtrlMgr

Generated struct type declarations for the Motor Control loop / RTE interface data; macros for access of Motor Control loop data
