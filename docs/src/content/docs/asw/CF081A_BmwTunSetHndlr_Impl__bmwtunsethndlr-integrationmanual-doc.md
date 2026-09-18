---
title: 'CF081A_BmwTunSetHndlr_Impl — BmwTunSetHndlr_IntegrationManual'
description: 'Converted .doc document BmwTunSetHndlr_IntegrationManual.doc from module CF081A_BmwTunSetHndlr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BmwTunSetHndlr_IntegrationManual.doc` (.doc, 136 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CF081A_BmwTunSetHndlr_Impl/doc/BmwTunSetHndlr_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Byrski, Krzysztof, Revision Number: 24, Name of Creating Application: Microsoft Office Word, Total Editing Time: 55:00, Create Time/Date: Thu Jul 17 09:54:00 2014, Last Saved Time/Date: Thu May 17 11:45:00 2018, Number of Pages: 12, Number of Words: 766, Number of Characters: 4367, Security: 0; recovered text fragments: 299

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- BmwTunSetHndlr
- VERSION: 21.0
- DATE: 2717-MARMAY-2018
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

Krzysztof Byrski

27-MJar-2018

Updated to Design 3.0.0

17-May-2018

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

EA4 Software Naming Conventions

Software Design and Coding Standards

CF081A_BmwTunSetHndlr_Design

See Synergy Sub Project Version

Dependencies

Module

Required Feature
