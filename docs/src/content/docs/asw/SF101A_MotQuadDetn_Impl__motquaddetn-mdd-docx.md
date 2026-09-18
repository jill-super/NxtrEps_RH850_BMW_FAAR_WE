---
title: 'SF101A_MotQuadDetn_Impl — MotQuadDetn_MDD'
description: 'Converted Word (.docx) document MotQuadDetn_MDD.docx from module SF101A_MotQuadDetn_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotQuadDetn_MDD.docx` (Word (.docx), 79 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 2 (png); OLE embeddings: 0; tables converted: 8

## Converted content

Module Design Document

For

Motor Quadrant Detection

VERSION: 1.0

DATE:  11-MAY-2015

Prepared By:

Shawn Penning

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1.0 | 11-May-2015 |

| 2 | Update to Unit Test Considerations | SPP | 2.0 | 16-Jun-2017 |



Table of Contents

1Abbrevations And Acronyms5

2References6

3motquaddetn & High-Level Description7

4Design details of software module8

4.1Graphical representation of  MOtquaddetn8

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

6.1.1.2Global10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation11

7.1Sub-Module Functions11

7.1.1Initialization Functions11

7.1.1.1INIT: MotQuadDetnInit111

7.1.1.2Design Rationale11

7.1.1.3Store Module Inputs to Local copies11

7.1.1.4(Processing of function)………11

7.1.1.5Store Local copy of outputs into Module Outputs11

7.1.2PERIODIC FUNCTIONS11

7.1.2.1Per: MotQuadDetnPer111

7.1.2.2Design Rationale11

7.1.2.3Store Module Inputs to Local copies11

7.1.2.4(Processing of function)………11

7.1.2.5Store Local copy of outputs into Module Outputs11

7.2Interrupt Functions11

7.3Serial Communication Functions12

7.4Local Function/Macro Definitions12

7.5GLObAL Function/Macro Definitions12

7.6TRANSIENT FUNCTIONS12

8Known Limitations With Design13

9UNIT TEST CONSIDERATION14

10Appendix15

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  | <ADD more to the table if applicable> |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| <1> | <MDD Guidelines> | Process 3.06.00 |

| <2> | <Software Naming Conventions> | Process 3.06.00 |

| <3> | <Coding standards> | Process 3.06.00 |

| <4> | FDD – SF101A Motor Quadrant Detection | See Synergy Subproject version |

|  | <Add if more available> |  |



## motquaddetn & High-Level Description

None

## Design details of software module

### Graphical representation of  MOtquaddetn

### Data Flow Diagram

### Module level DFD

N/A

### Sub-Module level DFD

N/A

### COMPONENT FLOW DIAGRAM

N/A

## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>



| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| N/A |  |  |  |  |



### Variable definition for enumerated types



| Enum Name | Element Name | Value |

| --- | --- | --- |

| N/A |  |  |



## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

< All program specific constants will be defined in detail >

### Local



| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer constants from .m file |  |  |  |



### Global

<This section lists the global constants used by the module.  For details on global constants, refer to the Data Dictionary for the application>



| Constant Name |

| --- |

| N/A |



### Module specific Lookup Tables Constants

<(This is for lookup tables (arrays) with fixed values, same name as other tables)>



| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

| <Refer Constant name qualified in [2]> | <Refer MDD guidelines [1]> | <Refer MDD guidelines [1]> | <Refer MDD guidelines [1]> |



## Software Module Implementation

### Sub-Module Functions

None

### Initialization Functions

### INIT: MotQuadDetnInit1

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### PERIODIC FUNCTIONS

(Note: For multiple periodic functions, insert new headers at the “Header 2” level – subset of “7.2 Periodic Functions” and follow the same sub-section design shown below).   If none required, place the text “None”)>

### Per: MotQuadDetnPer1

### Design Rationale

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Serial Communication Functions

None

### Local Function/Macro Definitions

None

### GLObAL Function/Macro Definitions

None

### TRANSIENT FUNCTIONS

None

## Known Limitations With Design

Rollover Checking is not needed. Fixed point math implementation takes care of it and no additional logic is required.

## UNIT TEST CONSIDERATION

- Rollovers should not occur in normal operation in the vehicle, however, rollovers will most likely occur during dynamometer testing or other tests. (From Motor Control FDD REPS GG4500 BMW 5.3.doc)

## Appendix

None
