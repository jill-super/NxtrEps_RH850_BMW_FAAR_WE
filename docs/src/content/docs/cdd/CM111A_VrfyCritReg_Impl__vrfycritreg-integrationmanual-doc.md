---
title: 'CM111A_VrfyCritReg_Impl — VrfyCritReg_IntegrationManual'
description: 'Converted .doc document VrfyCritReg_IntegrationManual.doc from module CM111A_VrfyCritReg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `VrfyCritReg_IntegrationManual.doc` (.doc, 156 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM111A_VrfyCritReg_Impl/doc/VrfyCritReg_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Avinash James, Revision Number: 41, Name of Creating Application: Microsoft Office Word, Total Editing Time: 21:56:00, Create Time/Date: Wed Jul  1 18:52:00 2015, Last Saved Time/Date: Wed May 24 18:04:00 2017, Number of Pages: 12, Number of Words: 1015, Number of Characters: 5788, Security: 0; recovered text fragments: 335

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- VrfyCritReg
- VERSION: 34.0
- DATE: 2022-FebMay-2017
- Prepared By:
- Sankardu VaradapureddiSoftware Group,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description

Author

Version

Initial version

Sankardu Varadapureddi

14-Jan-2016

Updated to

Critical register

checks at init and periodic functions

Selva Sengottaiyan

14-Apr-2016

Updated for micro diag special build parameter

Avinash James

20-Feb-2017

Added support for MCAl write verify feature

22-May-2017

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
