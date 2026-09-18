---
title: 'SF014A_InertiaCmpVel_Impl — InertiaCmpVel_IntegrationManual'
description: 'Converted Word (.docx) document InertiaCmpVel_IntegrationManual.docx from module SF014A_InertiaCmpVel_Impl.'
sidebar:
  hidden: true
---

> **Source:** `InertiaCmpVel_IntegrationManual.docx` (Word (.docx), 78 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

InertiaCmpVel

VERSION: 1.0

DATE: 23-Jul-2015

Prepared By:

Spandana Balani

Nexteer Automotive,

Saginaw, MI, USA

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | SB | 1.0 | 23-July-2015 |



Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3Da Vinci Parameter Configuration Changes7

4.4DaVinci Interrupt Configuration Changes7

4.5Manual Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

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

| <1> | <MDD Guidelines> | Process 4.01.00 |

| <2> | <Software Naming Conventions> | Process 4.01.00 |

| <3> | <Coding standards> | Process 4.01.00 |

| <4> | FDD – SF014A_InertiaCmpVel_Design | See Synergy Subproject version |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None |  |



### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| FLTINJENA | Set to STD_ON for Fault injection |  |



### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes



| Parameter | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |



### DaVinci Interrupt Configuration Changes



| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| N/A |  |  |  |



### Manual Configuration Changes



| Constant | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |



## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

No

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| InertiaCmpVelInit1 | On Init | RTE_Init |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| InertiaCmpVelPer1 | None | RTE(2ms) |



.

## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |



Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None
