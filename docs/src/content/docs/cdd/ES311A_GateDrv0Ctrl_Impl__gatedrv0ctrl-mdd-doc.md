---
title: 'ES311A_GateDrv0Ctrl_Impl — GateDrv0Ctrl_MDD'
description: 'Converted .doc document GateDrv0Ctrl_MDD.doc from module ES311A_GateDrv0Ctrl_Impl.'
sidebar:
  hidden: true
---

> **Source:** `GateDrv0Ctrl_MDD.doc` (.doc, 474 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES311A_GateDrv0Ctrl_Impl/doc/GateDrv0Ctrl_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Shawn Penning, Revision Number: 3, Name of Creating Application: Microsoft Office Word, Total Editing Time: 03:00, Create Time/Date: Fri Jan 12 18:18:00 2018, Last Saved Time/Date: Fri Jan 12 18:21:00 2018, Number of Pages: 16, Number of Words: 2562, Number of Characters: 14605, Security: 0; recovered text fragments: 265

## Converted content

## Document outline (extracted text fragments)

- bjbj	@	@
- Module Design Document
- Gate Drive 0 Control
- VERSION: 89
- DATE: 1112-SepJan-20172018
- Prepared By:
- Shruthi RaghavanShawn Penning,
- Nexteer Automotive,
- Saginaw, MI, USA
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Version

Description

Author

Initial version

Rijvi Ahmed

07-July-2016

Updated to design revision 1.8.0

Avinash James

21-Jan-2017

Updated to design revision 2.0.0

Shruthi Raghavan

17-Feb-2017

Updated to design revision 2.1.0

27-Feb-2017

Updated to design revision 2.3.0

14-Mar-2017

Updated to design revision 2.4.0

Fix for phase reasonableness issues found during integration

24-Mar-2017

Removed unused inputs from OperFltMonSt function.

Added UT considerations per anomaly EA4#11845

26-May-2017

Updated graphical representation for the new outputs and client call. Added details for changed & new local functions

Added new enum type and local constant

11-Sep-2017

Updated design rationale for the state machine in Configuration State of gate drive. Added UT considerations per test corrections required in anomaly corrective action.

Shawn Penning

12-Jan-2018

Table of Contents

1	Abbrevations And Acronyms

2	References

3	GATEDRV0CTRL & High-Level Description

4	Design details of software module

4.1	Graphical representation of GATEDRV0CTRL

5	Variable Data Dictionary

5.1	User defined typedef definition/declaration

5.2	Variable definition for enumerated types

6	Constant Data Dictionary

6.1	Program(fixed) Constants

6.1.1	Embedded Constants

6.1.1.1	Local

6.1.1.2	Global

6.1.2	Module specific Lookup Tables Constants

7	Software Module Implementation

7.1	Sub-Module Functions

7.2	Initialization Functions

7.2.1	Per: GateDrv0CtrlInit1

7.3	PERIODIC FUNCTIONS

7.3.1	Per: GateDrv0CtrlPer1
