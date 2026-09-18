---
title: 'CM101A_ExcpnHndlg_Impl — ExcpnHndlg Integration Manual'
description: 'Converted .doc document ExcpnHndlg Integration Manual.doc from module CM101A_ExcpnHndlg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `ExcpnHndlg Integration Manual.doc` (.doc, 148 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM101A_ExcpnHndlg_Impl/doc/ExcpnHndlg Integration Manual.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Avinash James, Revision Number: 48, Name of Creating Application: Microsoft Office Word, Total Editing Time: 06:23:00, Create Time/Date: Thu Jul 17 15:54:00 2014, Last Saved Time/Date: Wed Apr  4 16:36:00 2018, Number of Pages: 13, Number of Words: 1506, Number of Characters: 8587, Security: 0; recovered text fragments: 342

## Converted content

## Document outline (extracted text fragments)

- Integration Manual
- ExcpnHndlg
- VERSION: 78
- DATE: 0904/2104/1718
- Prepared By:
- Shruthi Raghavan,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Sl.No.
- Description

Author

Version

Initial version

Lucas Wendling

01/19/16

Updated for ChkForStrtUpTest() functions and Clock Monitor FE

Avinash James

02/10/16

Updated for DTS RAM Double bit ECC error from FENMI to SYSERR

03/22/16

Updates for New FENMI Handlers for mode error and removed SPI Dbt Bit handler

04/05/16

Updates to build time config paramters

03/02/17

Updates to add configuration for name of WdgMgr configuration structure

Shruthi Raghavan

05/25/17

Added NVM for storing debug info

09/21/17

Added global function FeNmiDtsEccSngBitErr

04/04/18

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
