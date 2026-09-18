---
title: 'ES102A_PolarityCfg_Impl — PolarityCfg_Integration Manual'
description: 'Converted Word (.docx) document PolarityCfg_Integration Manual.docx from module ES102A_PolarityCfg_Impl.'
sidebar:
  hidden: true
---

> **Source:** `PolarityCfg_Integration Manual.docx` (Word (.docx), 78 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

‘PolarityCfg’

VERSION: 1.0

DATE: 26-May-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Sankardu Varadapureddi | 1.0 | 26-May-2015 |



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

| 1 | FDD – ES102A_PolarityCfg_Design | See Synergy sub project version |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding Standards | Process 3.06.00 |



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

No

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| PolarityCfgInit1 | None | Init |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| PolarityCfgRead_Oper PolarityCfgWr_Oper |  | On event On event |



## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |



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
