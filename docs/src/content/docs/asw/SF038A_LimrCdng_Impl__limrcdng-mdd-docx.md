---
title: 'SF038A_LimrCdng_Impl — LimrCdng_MDD'
description: 'Converted Word (.docx) document LimrCdng_MDD.docx from module SF038A_LimrCdng_Impl.'
sidebar:
  hidden: true
---

> **Source:** `LimrCdng_MDD.docx` (Word (.docx), 106 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'Module Design Document', 'creator': 'Nexteer Employee', 'subject': '', 'keywords': '', 'description': ''}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 3

## Converted content

For

LimrCdng

July 22, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History



| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | N. Saxton | 1.0.0 | 22-Jul-2015 |



Table of Contents

1LimrCdng High-Level Description4

2Design details of software module5

2.1Graphical representation of LimrCdng5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1.1Sub-Module Functions7

4.1.2Interrupt Service Routines7

4.1.3Server Runnable Functions7

4.1.4Module Internal (Local) Functions7

4.1.5Transition Functions7

5Known Limitations with Design8

6UNIT TEST CONSIDERATION9

Appendix AAbbreviations and Acronyms10

Appendix BGlossary11

Appendix CReferences12

## LimrCdng High-Level Description

This function provides a layer of protection from erroneous signals feeding into SF04 Sum & Limit. It is applied primarily to limiting signals that serve to reduce motor torque command under certain operating conditions. This function can prevent step response or toggling behavior that might cause undesirable vehicle feel. It includes fault injection capability at some inputs to facilitate tuning.

## Design details of software module

Refer FDD

### Graphical representation of LimrCdng

### Data Flow Diagram

Refer FDD

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer .m file

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {_Init()}

None

#### Periodic sub-module {LimrCdngPer1}

Refer FDD

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

None

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms

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

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | SF038A LimrCdng FDD | See Synergy subproject version |
