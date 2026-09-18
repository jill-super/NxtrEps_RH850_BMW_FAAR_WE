---
title: 'ES002A_McuDiagc_Impl — McuDiagc_IntegrationManual'
description: 'Converted Word (.docx) document McuDiagc_IntegrationManual.docx from module ES002A_McuDiagc_Impl.'
sidebar:
  hidden: true
---

> **Source:** `McuDiagc_IntegrationManual.docx` (Word (.docx), 78 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

McuDiagc

VERSION: 4.0

DATE: 10-Dec-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva | 1.0 | 29-Mar-2016 |

| 2 | Added diagnostic for 2 milli second to Motor Control | Avinash James | 2.0 | 22-Jun-2016 |

| 3 | Optimized the diagnostic and removed periodic 3 | Avinash James | 3.0 | 28-Sep-2016 |

| 4 | Added micro diag error injection build config param | Avinash James | 4.0 | 10-Dec-2016 |



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

| FDD | Functional Design Document |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD – ES002A McuDiagc | See Synergy subproject version |

| 2 | Software Naming Conventions | Process 04.02.01 |

| 3 | Software Coding Standards | Process 04.02.01 |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None |  |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| MCUDIAGCERRINJ | STD_OFF for other builds STD_ON for uDiag test builds |  |



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

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.



| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagcInit1 | None | RTE (Init) |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagcPer1 | None | MotorControl ISR*2 |

| McuDiagcPer2 | None | RTE (2 ms) |



## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotCtrl_START_SEC_CODE | Code section for Motor Control scheduled functions | Constants are defined at function level. Memory mapping need to be adjusted accordingly. |



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
