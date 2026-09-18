---
title: 'CM475A_TSG31CfgAndUse_Impl — TSG31CfgAndUse_MDD'
description: 'Converted .doc document TSG31CfgAndUse_MDD.doc from module CM475A_TSG31CfgAndUse_Impl.'
sidebar:
  hidden: true
---

> **Source:** `TSG31CfgAndUse_MDD.doc` (.doc, 236 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: CM475A_TSG31CfgAndUse_Impl/doc/TSG31CfgAndUse_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Avinash James, Revision Number: 21, Name of Creating Application: Microsoft Office Word, Total Editing Time: 08:43:00, Create Time/Date: Tue Apr 28 12:57:00 2015, Last Saved Time/Date: Fri Jan 26 15:27:00 2018, Number of Pages: 17, Number of Words: 2078, Number of Characters: 11847, Security: 0; recovered text fragments: 292

## Converted content

## Document outline (extracted text fragments)

- TSG31 Timer Subsystem Configuration and Use
- Module Design Document
- VERSION: 23.0
- DATE:  2025-JunJan-20152018
- Revision History
- Description
- Author
- Version
- Initial Version
- K. Creager
- 28-Apr-2015
- Remove CnvNanoSecToHalfTmrCnt() function and add masking constant for changes in FDD ver 1.3.0

20-Jun-2015

Added MissUpdtCntrDiagc local function and updated parameters in NoTranSysStNotEn

Avinash James

25-Jan-2018

Table of Contents

1	Abbrevations And Acronyms

2	References

3	TSG31CfgAndUse High-Level Description

3.1	Design details of software module

3.2	Graphical representation of CDD_TSG31CfgAndUse

3.3	Data Flow Diagram

3.3.1	Module level DFD

3.3.2	Sub-Module level DFD

3.4	COMPONENT FLOW DIAGRAM

4	Variable Data Dictionary

4.1	User defined typedef definition/declaration

4.2	Variable definition for enumerated types

5	Constant Data Dictionary

5.1	Program(fixed) Constants

5.1.1	Embedded Constants

5.1.1.1	Local

5.1.1.2	Global

5.1.2	Module specific Lookup Tables Constants

6	Software Module Implementation

6.1	Sub-Module Functions

6.1.1	Motor Control Periodic: TSG31CfgAndUsePer1

6.1.1.1	Design Rationale

6.2	Initialization Functions

6.2.1	Init: TSG31CfgAndUseInit1

6.2.1.1	Design Rationale

6.2.1.2	Module Outputs

6.2.1.3	Module Internal

6.3	PERIODIC FUNCTIONS

6.3.1	Per: TSG31CfgAndUsePer2

6.3.1.1	Design Rationale

6.3.1.2	Store Module Inputs to Local copies

6.3.1.3	(Processing of function)

6.3.1.4	Store Local copy of outputs into Module Outputs

6.4	Interrupt Functions

6.5	Serial Communication Functions

6.6	Local Function/Macro Definitions

6.6.1	Local Function #1

6.6.1.1	Description

6.6.2	Local Function #2

6.6.2.1	Description

6.6.3	Local Function #3

6.6.3.1	Description

6.6.4	Local Function #4
