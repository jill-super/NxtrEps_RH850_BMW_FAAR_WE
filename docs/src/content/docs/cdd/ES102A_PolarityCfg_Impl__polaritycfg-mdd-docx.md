---
title: 'ES102A_PolarityCfg_Impl — PolarityCfg_MDD'
description: 'Converted Word (.docx) document PolarityCfg_MDD.docx from module ES102A_PolarityCfg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PolarityCfg_MDD.docx` (Word (.docx), 112 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 3 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Module Design Document

For

‘PolarityCfg’

VERSION: 3.0

DATE: 07-Jul-2017

Prepared By:

Shawn Penning,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sankardu Varadapureddi | 1.0 | 26-May-2015 |

| 3 | Corrections to Name and Graphic, Update MDD Layout | Shawn Penning | 3.0 | 07-Jul-2017 |



Table of Contents

1Polarity Configuration High-Level Description6

2Design details of software module7

2.1Graphical representation of Polarity Configuration7

2.2Data Flow Diagram7

2.2.1Module level DFD7

2.2.2Sub-Module level DFD7

2.3COMPONENT FLOW DIAGRAM8

3Variable Data Dictionary9

3.1User defined typedef definition/declaration9

3.2Variable definition for enumerated types9

4Constant Data Dictionary10

4.1Program(fixed) Constants10

4.1.1Embedded Constants10

4.1.1.1Local10

4.1.1.2Global10

4.1.2Module specific Lookup Tables Constants10

5Software Module Implementation11

5.1Sub-Module Functions11

5.1.1Initialization Functions11

5.1.1.1INIT: PolarityCfgInit11

5.1.1.1.1Design Rationale11

5.1.1.1.2Module Outputs11

5.1.1.1.3Module Internal11

5.1.2PERIODIC FUNCTIONS11

5.1.3Interrupt Functions11

5.1.4Server runnables12

5.1.4.1PolarityCfgRead12

5.1.4.1.1Design Rationale12

5.1.4.1.2Store Module Inputs to Local copies12

5.1.4.1.3(Processing of function)………12

5.1.4.1.4Store Local copy of outputs into Module Outputs12

5.1.4.2PolarityCfgWr12

5.1.4.2.1Design Rationale12

5.1.4.2.2Store Module Inputs to Local copies12

5.1.4.2.3(Processing of function)………12

5.1.4.2.4Store Local copy of outputs into Module Outputs12

5.1.5Local Function/Macro Definitions12

5.1.5.1Local Function #112

5.1.5.2Description12

5.1.6GLObAL Function/Macro Definitions13

5.1.7Transition FUNCTIONS13

6Known Limitations With Design14

7UNIT TEST CONSIDERATION15

Appendix A  Abbreviations and Acronyms16

Appendix B  Glossary17

Appendix C  References18

This section lists the title & version of all the documents that are referred for development of this document

## Polarity Configuration High-Level Description

This function will identify polarity control settings for certain points in the design.

## Design details of software module

### Graphical representation of Polarity Configuration

### Data Flow Diagram

Refer FDD

### Module level DFD

Refer FDD

### Sub-Module level DFD

Refer FDD

### COMPONENT FLOW DIAGRAM

Refer FDD

## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None |  |  |  |  |



### Variable definition for enumerated types



| Enum Name | Element Name | Value |

| --- | --- | --- |

| None |  |  |



## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| HWAG0POL_CNT_U32 | Bitfield Mask | NA | 0x00000001U |

| HWAG1POL_CNT_U32 | Bitfield Mask | NA | 0x00000002U |

| HWAG2POL_CNT_U32 | Bitfield Mask | NA | 0x00000004U |

| HWAG3POL_CNT_U32 | Bitfield Mask | NA | 0x00000008U |

| HWAG4POL_CNT_U32 | Bitfield Mask | NA | 0x00000010U |

| HWAG5POL_CNT_U32 | Bitfield Mask | NA | 0x00000020U |

| HWAG6POL_CNT_U32 | Bitfield Mask | NA | 0x00000040U |

| HWAG7POL_CNT_U32 | Bitfield Mask | NA | 0x00000080U |

| HWTQ0POL_CNT_U32 | Bitfield Mask | NA | 0x00000100U |

| HWTQ1POL_CNT_U32 | Bitfield Mask | NA | 0x00000200U |

| HWTQ2POL_CNT_U32 | Bitfield Mask | NA | 0x00000400U |

| HWTQ3POL_CNT_U32 | Bitfield Mask | NA | 0x00000800U |

| HWTQ4POL_CNT_U32 | Bitfield Mask | NA | 0x00001000U |

| HWTQ5POL_CNT_U32 | Bitfield Mask | NA | 0x00002000U |

| HWTQ6POL_CNT_U32 | Bitfield Mask | NA | 0x00004000U |

| HWTQ7POL_CNT_U32 | Bitfield Mask | NA | 0x00008000U |

| MOTAGMECL0POL_CNT_U32 | Bitfield Mask | NA | 0x00010000U |

| MOTAGMECL1POL_CNT_U32 | Bitfield Mask | NA | 0x00020000U |

| MOTAGMECL2POL_CNT_U32 | Bitfield Mask | NA | 0x00040000U |

| MOTAGMECL3POL_CNT_U32 | Bitfield Mask | NA | 0x00080000U |

| MOTAGMECL4POL_CNT_U32 | Bitfield Mask | NA | 0x00100000U |

| MOTAGMECL5POL_CNT_U32 | Bitfield Mask | NA | 0x00200000U |

| MOTAGMECL6POL_CNT_U32 | Bitfield Mask | NA | 0x00400000U |

| MOTAGMECL7POL_CNT_U32 | Bitfield Mask | NA | 0x00800000U |



### Global



| Constant Name |

| --- |



### Module specific Lookup Tables Constants



| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

| None |  |  |  |



## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

PolarityCfgInit

### INIT: PolarityCfgInit

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Refer ‘PolarityCfgInit’ block in FDD

### Module Internal

None

### PERIODIC FUNCTIONS

None

### Interrupt Functions

None

### Server runnables

### PolarityCfgRead

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer ‘PolarityCfgRead’ block in FDD

### Store Local copy of outputs into Module Outputs

None

### PolarityCfgWr

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer  ‘PolarityCfgWr’ block in FDD

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

### Local Function #1



| Function Name | GetPolarity | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Polarity_Cnt_T_u32 | uint32 | 0 | 0xFFFFFFFF |

|  | PolarityMask_Cnt_T_u32 | uint32 | 0x00000001 | 0x02000000 |

| Return Value | Polarity_Cnt_T_s08 | sint08 | -1 | 1 |



### Description

- Design:

- if ( (Polarity_Cnt_T_u32 & PolarityMask_Cnt_T_u32) == PolarityMask_Cnt_T_u32 )

set  ‘Polarity_Cnt_T_s08’ to ‘1’

else

set  ‘Polarity_Cnt_T_s08’ to ‘-1’

- Note:  ‘PolarityMask_Cnt_T_u32’ is a bit field mask and takes values mentioned in table at sec 6.1.1.1

### GLObAL Function/Macro Definitions

None

### Transition FUNCTIONS

None

## Known Limitations With Design

None

## UNIT TEST CONSIDERATION

None

## Appendix A  Abbreviations and Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |



## Appendix B  Glossary

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



## Appendix C  References



| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | EA4 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD : ES102A_PolarityCfg_Design | See Synergy sub project version |
