---
title: 'ES259B_BattVltgCorrln_Impl — BattVltgCorrln_IntegrationManual'
description: 'Converted .doc document BattVltgCorrln_IntegrationManual.doc from module ES259B_BattVltgCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `BattVltgCorrln_IntegrationManual.doc` (.doc, 140 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES259B_BattVltgCorrln_Impl/doc/BattVltgCorrln_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Brionna Spencer, Revision Number: 45, Name of Creating Application: Microsoft Office Word, Total Editing Time: 03:05:00, Create Time/Date: Mon Jun  8 18:04:00 2015, Last Saved Time/Date: Tue Jun 27 18:05:00 2017, Number of Pages: 12, Number of Words: 700, Number of Characters: 3990, Security: 0; recovered text fragments: 296

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- BattVltgCorrln
- VERSION: 1.02.0
- DATE: 25-MAY-201627-Jun-2017
- Prepared By:
- Nick SaxtonBrionna Spencer,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description

Author

Version

Initial version

N. Saxton

25-May-2016

Listed missing memory section in 7.1 Mapping.

B. Spencer

27-Jun-2017

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

ES259B Battery or Switched Voltage Correlation

See Synergy subproject version

EA4 Software Naming Conventions

01.01.00Process 4.01.0

Software Design and Coding Standards

Process 4.01.02.1
