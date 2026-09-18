---
title: 'ES101A_DiagcMgr_Impl — DiagcMgr_IntegrationManual'
description: 'Converted .doc document DiagcMgr_IntegrationManual.doc from module ES101A_DiagcMgr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `DiagcMgr_IntegrationManual.doc` (.doc, 225 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES101A_DiagcMgr_Impl/doc/DiagcMgr_IntegrationManual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shruthi Raghavan, Revision Number: 62, Name of Creating Application: Microsoft Office Word, Total Editing Time: 1d+12:07:00, Create Time/Date: Wed Nov 30 17:17:00 2016, Last Saved Time/Date: Thu May  4 20:59:00 2017, Number of Pages: 13, Number of Words: 2022, Number of Characters: 11526, Security: 0; recovered text fragments: 235

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- Diagnostic Manager
- VERSION: 67.0
- DATE: 0726-APRDEC-20167
- Prepared By:
- Software GroupShruthi Raghavan,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl. No.
- Description

Author

Version

Initial version

Spandana Balani

23-Apr-2015

Updated to FDD version 2

11-Mar-2016

Updated to FDD version 3

22-APR-2016

Updated to FDD version 4

22-Jun-2016

Added new parameter in configurator

30-Nov-2016

Remove Nvm block id for SnpshtDataAry

07-Dec-2016

Add Nvm block id for new LtchCntrAry NVM

Added runnable scheduling for added runnables

Shruthi Raghavan

26-APR-2017

Table of Contents

1	Abbrevations And Acronyms

2	References

3	Dependencies

3.1	SWCs

3.2	Global Functions(Non RTE) to be provided to Integration Project

4	Configuration REQUIREMeNTS

4.1	Build Time Config.

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
