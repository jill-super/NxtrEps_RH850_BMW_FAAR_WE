---
title: 'AR998A_NxtrDet_Impl — NxtrDet Module Design Document'
description: 'Converted Word (.docx) document NxtrDet Module Design Document.docx from module AR998A_NxtrDet_Impl.'
sidebar:
  hidden: true
---

> **Source:** `NxtrDet Module Design Document.docx` (Word (.docx), 90 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Windows User', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 7

## Converted content

For

NxtrDet

Oct 6, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Lucas Wendling | 1 | 10/06/15 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2NxtrDet High-Level Description5

3Design details of software module6

3.1Graphical representation of NxtrDet6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: NxtrDet8

5.1.2Per: NxtrDet8

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.4.1Local Function #18

5.4.1.1Design Rationale8

5.4.1.2Processing8

5.5GLOBAL Function/Macro Definitions8

5.5.1GLOBAL Function #18

5.5.1.1Design Rationale8

5.5.1.2Processing8

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## NxtrDet High-Level Description

See FDD

## Design details of software module

### Graphical representation of NxtrDet

None

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Constants containing the Nexteer ModuleIDs defined for Det functionality are defined in the .m file included in the doc folder of this component.  This is to allow new SWCs adding new Det errors to not drive changes to the design project, only to the implementation project.

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| None |  |  |  |



## Software Component Implementation

### Sub-Module Functions

### Init: NxtrDet

None

### Per: NxtrDet

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1



| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

| Return Value |  |  |  |  |



### Design Rationale

### Processing

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

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |
