---
title: 'ES100A_SysStMod_Impl — SysStMod_MDD'
description: 'Converted .doc document SysStMod_MDD.doc from module ES100A_SysStMod_Impl.'
sidebar:
  hidden: true
---

> **Source:** `SysStMod_MDD.doc` (.doc, 146 KB, in-module path `doc/`)
>
> Legacy binary Word format cannot be rendered directly by this static site. The outline below was recovered from the file metadata and embedded text strings; tables, diagrams and exact formatting are not preserved. See the source file in the repository for the authoritative content.
>
> file metadata: ES100A_SysStMod_Impl/doc/SysStMod_MDD.doc: Composite Document File V2 Document, Little Endian, Os: Windows, Version 6.1, Code page: 1252, Title: MDD Design Template V1.0, Author: Nexteer, Comments: version 1.0 dated 24-Dec-2013, Template: Normal.dotm, Last Saved By: Windows User, Revision Number: 2, Name of Creating Application: Microsoft Office Word, Create Time/Date: Tue Apr  5 13:08:00 2016, Last Saved Time/Date: Tue Apr  5 13:08:00 2016, Number of Pages: 13, Number of Words: 808, Number of Characters: 4611, Security: 0; recovered text fragments: 319

## Converted content

## Document outline (extracted text fragments)

- bjbjupup
- Module Design Document
- System States and Modes
- VERSION: 12
- DATE: 2505-MarApr-20152016
- Location: The official version of this document is stored in the Nexteer Configuration Management System.
- Revision History
- Version
- Description
- Author
- Initial version
- Owen Tosh

25-Mar-2015

Updated for FDD ver 1.3.0

Sankardu Varadapureddi

05-Apr-2016

Table of Contents

1	Abbrevations And Acronyms

2	References

3	SysStMod & High-Level Description

4	Design details of software module

4.1	Graphical representation of SysStMod

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

7.2.1	Init: SysStMd_Init1

7.2.1.1	Design Rationale

7.2.1.2	Module Internal

7.3	PERIODIC FUNCTIONS

7.3.1	Per: SysStMd_Per1

7.3.1.1	Design Rationale

7.3.1.2	Processing of Function

7.4	Interrupt Functions

7.5	Serial Communication Functions

7.6	Local Function/Macro Definitions

7.7	GLObAL Function/Macro Definitions

8	Known Limitations With Design

9	UNIT TEST CONSIDERATION

Abbrevations And Acronyms

Abbreviation

Design functional diagram

Module design Document

References

This section lists the title & version of all the documents that are referred for development of this document

Sr. No.

Title

MDD Guidelines

Process 03.05.00

Software Naming Conventions

Software Coding Standards

SysStMod & High-Level Description
