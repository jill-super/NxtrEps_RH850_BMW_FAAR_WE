---
title: 'CM103A_RamMem_Impl — RamMem_MDD'
description: 'Converted Word (.docx) document RamMem_MDD.docx from module CM103A_RamMem_Impl.'
sidebar:
  hidden: true
---

> **Source:** `RamMem_MDD.docx` (Word (.docx), 97 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Spencer, Brionna', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 10

## Converted content

For

RamMem

Version: 4.0

Release Date: 11-Jul-2018

Prepared By:

Software Engineering,

Nexteer Automotive,

Saginaw, MI, USA

Document Change History



| Version | Description | Author | Date |

| --- | --- | --- | --- |

| 1 | Initial Version | Selva Sengottaiyan | 06-Apr-2016 |

| 2 | Created local functions for reducing cyclometric complexity | Selva Sengottaiyan | 26-Jun-2016 |

| 3 | Changed SPI ECC handling from interrupt to polling | Avinash James | 23-Aug-2016 |

| 4 | Updated local function arguments to match code | Bri Spencer | 11-Jul-2018 |



Table of Contents

1RamMem & High-Level Description5

2Design details of software module6

2.1Graphical representation of RamMem6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: RamMemInit18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: RamMemPer18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function) …8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runnables8

4.2.1RamMemLclRamSngBitEcc8

4.2.1.1Design Rationale8

4.2.1.2(Processing of function) …8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions9

4.4.1Local Function #19

4.4.1.1Design Rationale9

4.4.1.2Processing9

4.4.2Local Function #29

4.4.2.1Design Rationale9

4.4.2.2Processing9

4.4.3Local Function #39

4.4.3.1Design Rationale9

4.4.3.2Processing9

4.4.4Local Function #410

4.4.4.1Design Rationale10

4.4.4.2Processing10

4.4.5Local Function #510

4.4.5.1Design Rationale10

4.4.5.2Processing10

4.5GLOBAL Function/Macro Definitions10

5Known Limitations with Design11

6UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## RamMem & High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of RamMem

### Data Flow Diagram

#### Component level DFD

None

#### Function level DFD

None

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| LCLRAMBASADR_CNT_U32 | 1 | Cnt | 0xFEB80000U |

| VLDADRTESTBITMASK_CNT_U32 | 1 | Cnt | 0xFFFE0000U |

| VLDADRTESTRES_CNT_U32 | 1 | Cnt | 0x00060000U |

| WORDLINEADRMASK_CNT_U32 | 1 | Cnt | 0xFFFFFF1FU |

| BNK0ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000001U |

| BNK1ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000002U |

| BNK2ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000004U |

| BNK3ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000008U |

| BNK0SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00000001U |

| BNK1SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00000100U |

| BNK2SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00010000U |

| BNK3SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x01000000U |



Also see FDD DataDict.m file for constant definitions.

## Software Component Implementation

### Sub-Module Functions

### Init: RamMemInit1

### Design Rationale

None

### Module Outputs

Refer to FDD

### Per: RamMemPer1

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function) …

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Server Runnables

### RamMemLclRamSngBitEcc

### Design Rationale

None

### (Processing of function) …

Refer to FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1



| Function Name | SpiEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

None

### Processing

Refer to FDD

### Local Function #2



| Function Name | FrEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

None

### Processing

Refer to FDD

### Local Function #3



| Function Name | CanEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | N/A |  |  |  |



### Design Rationale

None

### Processing

Refer to FDD

### Local Function #4



| Function Name | RamFailrModClassnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LclRamFailrAdr_Cnt_T_u32 | uint32 | 0 | 4294967295 |

|  | ErrClrMask_Cnt_T_u32 | uint32 | 0 | 4294967295 |

|  | SngBitErrMask_Cnt_T_u32 | uint32 | 0 | 4294967295 |

| Return Value | N/A |  |  |  |



### Design Rationale

None

### Processing

Refer to FDD

### Local Function #5



| Function Name | RamMemLclRamFailrChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LclRamFailrAdr_Cnt_T_u32 | uint32 | 0 | 4294967295 |

| Return Value | N/A |  |  |  |



### Design Rationale

None

### Processing

Refer to FDD

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

Local RAM single-bit PIM for address store will be overwritten for each bank; this can be avoided by defining PIMs for each memory block. Will be reviewed POST IVER build.

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms



| Abbreviation or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document |

| MDD | Module Design Document |

| DFD | Data Flow Diagram |



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

| 1 | AUTOSAR Specification of Memory Mapping | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 1.02 |

| 3 | EA4 Software Naming Conventions | 1.03 |

| 4 | Software Design and Coding Standards | 2.01 |

| 5 | FDD: CM103A_RamMem_Design | See Synergy subproject version |
