---
title: 'CM510A_MotAg3Meas_Impl — MotAg3Meas_IntegrationManual'
description: 'Converted .doc document MotAg3Meas_IntegrationManual.doc from module CM510A_MotAg3Meas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAg3Meas_IntegrationManual.doc` (.doc, 140 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM510A_MotAg3Meas_Impl/doc/MotAg3Meas_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal, Last Saved By: Shishir Nagendra Holenarasipura Lakshmikanth S, Revision Number: 25, Name of Creating Application: Microsoft Office Word, Total Editing Time: 42:00, Create Time/Date: Thu Jul 17 15:54:00 2014, Last Saved Time/Date: Fri Apr  6 13:53:00 2018, Number of Pages: 12, Number of Words: 680, Number of Characters: 3878, Security: 0; recovered text fragments: 296

## Converted content

## Document outline (extracted text fragments)

- bjbjv
- Integration Manual
- MotAg3Meas
- VERSION: 12.0
- DATE: 0705-NOVAPR-20186
- Prepared By:
- Shruthi Raghavan,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.

Description

Author

Version

Initial version

Shruthi Raghavan

11/7/16

Updated DaVinci configurable parameters

Shishir Holenarasipura

05-Apr-2018

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

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

MDD Guidelines

EA4 01.00.01

EA4 Software Naming Conventions

01.00.00

Software Design and Coding Standards

CM510A_MotAg3Meas_Design
