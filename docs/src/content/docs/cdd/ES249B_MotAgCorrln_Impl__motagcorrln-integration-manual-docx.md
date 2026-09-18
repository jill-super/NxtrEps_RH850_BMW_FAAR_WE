---
title: 'ES249B_MotAgCorrln_Impl — MotAgCorrln_Integration Manual'
description: 'Converted Word (.docx) document MotAgCorrln_Integration Manual.docx from module ES249B_MotAgCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `MotAgCorrln_Integration Manual.docx` (Word (.docx), 76 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

‘MotAgCorrln’

VERSION: 1.0

DATE: 01 JUN 2016

Prepared By:

Software Engineering,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Nick Saxton | 1.0 | 01-Jun-2016 |



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



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD – ES249B_MotAgCorrln_Design | See Synergy sub project version |

| 2 | Software Naming Conventions | Process 04.2.00 |

| 3 | Software Design and Coding Standards | Process 04.2.00 |



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

| FLTINJENA | Set Value to STD_ON to enable fault injection |  |



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

Refer DataDict.m file in the FDD

### Specific Include Path present

No

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotAgCorrlnInit1 | None | RTE |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotAgCorrlnPer1 | None | RTE (2ms) |



.

## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotAgCorrln_START_SEC_CODE |  |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| <Memmap usuage info> |  |  |



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
