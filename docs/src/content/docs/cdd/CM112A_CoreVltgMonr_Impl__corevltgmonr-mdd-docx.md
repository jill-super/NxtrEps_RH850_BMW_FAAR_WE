---
title: 'CM112A_CoreVltgMonr_Impl — CoreVltgMonr_MDD'
description: 'Converted Word (.docx) document CoreVltgMonr_MDD.docx from module CM112A_CoreVltgMonr_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CoreVltgMonr_MDD.docx` (Word (.docx), 95 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Shruthi Raghavan', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 8

## Converted content

For

CoreVtlgMonr

Aug 2, 2017

Version : 2.0

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version of Module Design Document for CoreVltgMonr | Shruthi Raghavan | 1.0 | 19-May-2017 |

| Made CVM start up test as an Init function | Avinash James | 2.0 | 02-Aug-2017 |



Table of Contents

1Introduction4

1.1Purpose4

2CoreVtlgMonr & High-Level Description5

3Design details of software module6

3.1Graphical representation of CoreVtlgMonr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: CoreVtlgMonrInit18

5.1.1.1Design Rationale8

5.1.2Per: <Component Name>_Per<n>8

5.1.2.1Design Rationale8

5.2Server Runables8

5.2.1PrphlVltgMonrStrtUpTestFlt8

5.2.1.1Design Rationale8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.4.1Local Function #18

5.4.1.1Design Rationale8

5.5GLOBAL Function/Macro Definitions8

5.5.1GLOBAL Function #19

5.5.1.1Design Rationale9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module design document for Core voltage Monitor.

## CoreVtlgMonr & High-Level Description

CoreVltgMonr component is a MCAL supporting function for startup test for CVM

## Design details of software module

### Graphical representation of CoreVtlgMonr

### Data Flow Diagram

Refer FDD Simulink Model.

#### Component level DFD

Refer FDD Simulink Model.

#### Function level DFD

Refer FDD Simulink Model.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| NODEBSTEP_CNT_U16 | 1 | Cnt | 0U |

| Refer .m file |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: CoreVtlgMonrInit1

### Design Rationale

### Init: CoreVtlgMonrInit2

### Design Rationale

### Per: <Component Name>_Per<n>

### Design Rationale

This SWC does not have any periodic

### Server Runables

### Interrupt Functions

None.

### Module Internal (Local) Functions

### Local Function #1



| Function Name | None. | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA | - | - | - |

| Return Value | NA | - | - | - |



### Design Rationale

NA

### GLOBAL Function/Macro Definitions

None

### GLOBAL Function #1



| Function Name | None. | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA | - | - | - |

| Return Value | NA | - | - | - |



### Design Rationale

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |



#### Glossary

Note: Terms and definitions from the source “Nexteer Automotive” take precedence over all other definitions of the same term.  Terms and definitions from the source “Nexteer Automotive” are formulated from multiple sources, including the following:

- ISO 9000

- ISO/IEC 12207

- ISO/IEC 15504

- Automotive SPICE® Process Reference Model (PRM)

- Automotive SPICE® Process Assessment Model (PAM)

- ISO/IEC 15288

- ISO 26262

- IEEE Standards

- SWEBOK

- PMBOK

- Existing Nexteer Automotive documentation



| Term | Definition | Source |

| --- | --- | --- |

| MDD | Module Design Document |  |

| DFD | Data Flow Diagram |  |



#### References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | Software Engineering Process 04.04.02 |

| 3 | Software Naming Conventions.doc | Software Engineering Process 04.04.02 |

| 4 | Software Design and Coding Standards.doc | Software Engineering Process 04.04.02 |
