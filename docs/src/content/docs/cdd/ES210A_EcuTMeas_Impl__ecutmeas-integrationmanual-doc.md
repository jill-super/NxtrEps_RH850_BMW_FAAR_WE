---
title: 'ES210A_EcuTMeas_Impl — EcuTMeas_IntegrationManual'
description: 'Converted .doc document EcuTMeas_IntegrationManual.doc from module ES210A_EcuTMeas_Impl.'
sidebar:
  hidden: true
---

> **Source:** `EcuTMeas_IntegrationManual.doc` (.doc, 158 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES210A_EcuTMeas_Impl/doc/EcuTMeas_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shruthi Raghavan, Revision Number: 13, Name of Creating Application: Microsoft Office Word, Total Editing Time: 34:00, Create Time/Date: Mon Mar 21 20:31:00 2016, Last Saved Time/Date: Wed Aug  9 14:25:00 2017, Number of Pages: 13, Number of Words: 961, Number of Characters: 5478, Security: 0; recovered text fragments: 366

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- ECU TEMPERATURE MEASUREMENT
- DOCPROPERTY  Module  \* MERGEFORMAT
- EcuTMeas
- VERSION: 2.0
- DOCPROPERTY  "Document Version"  \* MERGEFORMAT
- DATE:
- DOCPROPERTY  "Release Date"  \* MERGEFORMAT
- 09-AUG-2017
- 21-MAR-2016
- Prepared By:
- DOCPROPERTY  "Prepared By"  \* MERGEFORMAT

Shruthi Raghavan

Krishna Anne,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

Sl. No.

Description

Author

Version

Initial version

Spandana Balani

23-Mar-2015

ADC Hooks are added as input

21-Mar-2016

Added config params

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
