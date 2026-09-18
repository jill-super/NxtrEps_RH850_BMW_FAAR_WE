---
title: 'SF040A_MotVel_Impl — MotVel_MDD'
description: 'Converted Word (.docx) document MotVel_MDD.docx from module SF040A_MotVel_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotVel_MDD.docx` (Word (.docx), 83 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

Module Design Document

For

‘MotVel’

VERSION: 2.0

DATE:  25-Jul-2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Shawn Penning

Saginaw, MI

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Rijvi Ahmed | 1.0 | 12-April-2016 |

| 2 | Updated per design rev. 2.0.0 | TATA | 2.0 | 18-Nov-2016 |

| 3 | Updated per design rev. 2.1.0 | Shawn Penning | 3.0 | 25-Jul-2017 |



Table of Contents

1Abbrevations And Acronyms5

2References6

3MotVel & High-Level Description7

4Design details of software module8

4.1Graphical representation OF MotVel8

4.2Data Flow Diagram8

4.2.1Module level DFD8

4.2.2Sub-Module level DFD8

4.3COMPONENT FLOW DIAGRAM8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Constant Data Dictionary10

6.1Program(fixed) Constants10

6.1.1Embedded Constants10

6.1.1.1Local10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation11

7.1Sub-Module Functions11

7.1.1Initialization Functions11

7.1.2PERIODIC FUNCTIONS11

7.1.2.1INIT: MotVelPER111

7.1.2.1.1Design Rationale11

7.1.2.2Design Rationale11

7.1.2.3Store Module Inputs to Local copies11

7.1.2.4(Processing of function)………11

7.1.2.5Store Local copy of outputs into Module Outputs11

7.1.3PERIODIC FUNCTIONS11

7.1.3.1INIT: MotVelPER211

7.1.3.1.1Design Rationale11

7.1.3.2Design Rationale11

7.1.3.3Store Module Inputs to Local copies11

7.1.3.4(Processing of function)………11

7.1.3.5Store Local copy of outputs into Module Outputs11

7.1.4Interrupt Functions12

Server runnables12

7.1.4.1.1Store Local copy of outputs into Module Outputs12

7.1.4.2Local Function/Macro Definitions12

7.1.5GLObAL Function/Macro Definitions12

7.1.6Tranisition FUNCTIONS12

8Known Limitations With Design13

9UNIT TEST CONSIDERATION14

10Appendix15

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | MDD Guidelines | Process 04.02.01 |

| 2 | Software Naming Conventions | Process 04.02.01 |

| 3 | Software Design and Coding standards | Process 04.02.01 |

| 4 | FDD : SF40A_MotVel_Design | See Synergy sub project version |



## MotVel & High-Level Description

- Please refer FDD.

## Design details of software module

### Graphical representation OF MotVel

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



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None | N/A | N/A | N/A | N/A |



### Variable definition for enumerated types



| Enum Name | Element Name | Value |

| --- | --- | --- |

| None | N/A | N/A |



## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer the m files |  |  |  |



6.1.1.2       Global



| Constant Name |

| --- |

| N/A |



### Module specific Lookup Tables Constants



| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

| None | N/A | N/A | N/A |



## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

None

### PERIODIC FUNCTIONS

### INIT: MotVelPER1

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### PERIODIC FUNCTIONS

### INIT: MotVelPER2

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Server runnables

None

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

- None

### GLObAL Function/Macro Definitions

None

### Tranisition FUNCTIONS

None

## Known Limitations With Design

- Per-Instance Memory variables in Design 2.1, MotAgBufIdxPrev and MotAgBufIdxPrim, are set with range of 0 to 255, but are index variables for an array of only 8 elements. Design to be corrected in the next version as follows:  the Max Value for both PIM’s to be 7 instead of 255 (range 0..7 instead of 0..255).

## UNIT TEST CONSIDERATION

Per-Instance Memory variables in Design 2.1, MotAgBufIdxPrev and MotAgBufIdxPrim, are set with range of 0 to 255, but are index variables for an array of only 8 elements. Design to be corrected in the next version as follows:  the Max Value for both PIM’s to be 7 instead of 255 (range 0..7 instead of 0..255).

## Appendix

None
