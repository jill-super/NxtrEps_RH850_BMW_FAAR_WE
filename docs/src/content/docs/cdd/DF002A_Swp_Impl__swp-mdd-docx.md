---
title: 'DF002A_Swp_Impl — Swp_MDD'
description: 'Converted Word (.docx) document Swp_MDD.docx from module DF002A_Swp_Impl.'
sidebar:
  hidden: true
---

> **Source:** `Swp_MDD.docx` (Word (.docx), 111 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Anne, Krishna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 5

## Converted content

For

Swp

Jan 20, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Kanth Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | 1.0.0 | 20-Oct-2015 |

| Fix for anomaly EA4#2461 | Krishna Kanth Anne | 1.1.0 | 20-Jan-2016 |



Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2PullCmpActv & High-Level Description5

3Design details of software module6

3.1Graphical representation of PullCmpActv6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: SwpInit18

5.1.2Per: SwpPer18

5.1.3Per: SwpPer28

5.2Module Internal (Local) Functions8

5.2.1Local Function #18

5.2.1.1Design Rationale8

5.2.1.2Processing8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

MDD for Sweep function

### Scope

NA

## Swp & High-Level Description

Please refer FDD.

## Design details of software module

Please refer FDD.

### Graphical representation of Swp

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer DF002A_Swp_DataDict.m | NA | NA | NA |

| SWPSTRT_CNT_U16 | NA | NA | 0 |

| SWPTRAN_CNT_U16 | NA | NA | 1 |

| SWPDWELL_CNT_U16 | NA | NA | 2 |

| SWPSTOP_CNT_U16 | NA | NA | 3 |

| SWPRAMP_CNT_U16 | NA | NA | 4 |

| SWPDONE_CNT_U16 | NA | NA | 5 |



## Software Component Implementation

Please refer FDD.

### Sub-Module Functions

### Init: SwpInit1

Please refer FDD.

### Design Rationale

Dummy Initialization function to correlate with the FDD (.m file)

### Per: SwpPer1

Please refer FDD.

### Design Rationale

- For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process. This is to give control over MemMap to avoid MPU violations while writing these variables using xcp.

- All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

- Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

- Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

### Per: SwpPer2

Please refer FDD.

### Design Rationale

- For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process. This is to give control over MemMap to avoid MPU violations while writing these variables using xcp.

- All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

- Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

- Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

- Please refer Init.txt file in the FDD design: DF002A_Swp_Design for initial values of Function level and Module level variables.

- For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process.

- All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

- Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

- Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

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

| 5 | FDD: SF002A_Swp_Design | See Synergy SubProject version |
