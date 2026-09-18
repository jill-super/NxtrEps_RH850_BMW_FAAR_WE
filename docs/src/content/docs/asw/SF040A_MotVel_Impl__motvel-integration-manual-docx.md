---
title: 'SF040A_MotVel_Impl — MotVel_Integration Manual'
description: 'Converted Word (.docx) document MotVel_Integration Manual.docx from module SF040A_MotVel_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotVel_Integration Manual.docx` (Word (.docx), 78 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

‘MotVel’

VERSION: 1.0

DATE: 12-April-2016

Prepared By:

Software Group

Nexteer Automotive,

Saginaw, MI, USA

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Rijvi Ahmed | 1.0 | 12-April-2016 |



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

7.3Non  RTE NvM Blocks10

7.4RTE NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms



| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD – SF40A_MotVel_Design | See Synergy sub project version |

| 2 | Software Naming Conventions | Process 04.02.01 |

| 3 | Software Design and Coding Standards | Process 04.02.01 |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None |  |



### Global Functions(Non RTE) to be provided to Integration Project

MotVelPer1

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| None |  |  |



### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes



| Parameter | Notes | SWC |

| --- | --- | --- |

| None |  |  |



### DaVinci Interrupt Configuration Changes



| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| None |  |  |  |



### Manual Configuration Changes



| Constant | Notes | SWC |

| --- | --- | --- |

| None |  |  |



## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file in the FDD

### Required Global Data Outputs

Refer DataDict.m file file in the FDD

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotVelInit1 | None | RTE/Init |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotVelPer1 | None | Motor Control ISR |

| MotVelPer2 | None | RTE/2ms |



## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotCtrl_START_SEC_CODE | Code section for Motor Control scheduled functions |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| <Memmap usuage info> |  |  |



Table 1: ARM Cortex R4 Memory Usage

### Non  RTE NvM Blocks

### RTE NvM Blocks

## Compiler Settings

### Preprocessor MACRO

None.

### Optimization Settings

None

## Appendix

None
