---
title: 'ES209B_CurrMeasCorrln_Impl — CurrMeasCorrln_IntegrationManual'
description: 'Converted Word (.docx) document CurrMeasCorrln_IntegrationManual.docx from module ES209B_CurrMeasCorrln_Impl.'
sidebar:
  hidden: true
---

> **Source:** `CurrMeasCorrln_IntegrationManual.docx` (Word (.docx), 72 KB, in-module path `doc/`)
>
> Converted from OOXML (`word/document.xml`); headings, lists and tables preserved. Embedded objects and images are inventoried below.
>
> props: {'title': 'MDD Design Template V1.0', 'creator': 'Nexteer', 'subject': '', 'keywords': '', 'description': 'version 1.0 dated 24-Dec-2013'}; embedded images: 1 (png); OLE embeddings: 0; tables converted: 12

## Converted content

Integration Manual

For

CURRENT MEASUREMENT CORRELATION

VERSION: 3.0

DATE: 07-Jun-2017

Prepared By:

Shawn Penning,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History



| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Nick Saxton | 1.0 | 26-Apr-2016 |

| 2 | Added FltInj point for an output | Krishna Anne | 2.0 | 27-Jun-16 |

| 3 | Added Init Runnable | Shawn Penning | 3.0 | 06-Jun-2017 |



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

|  | <ADD more to the table if applicable> |



## References

This section lists the title & version of all the documents that are referred for development of this document



| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD - ES209A Current Measurement Correlation | Refer current Synergy subproject version |

| 2 | Software Naming Conventions | 1.01.00 |

| 3 | Software Design and Coding Standards | 2.1 |



## Dependencies

### SWCs



| Module | Required Feature |

| --- | --- |

| None | N/A |



Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config



| Modules | Notes |  |

| --- | --- | --- |

| CurrMeasCorrln | FLTINJENA should be set to STD_ON as required |  |



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

| CurrMeasCorrlnInit1 | None | RTE Init |





| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CurrMeasCorrlnPer1 | None | RTE 2ms |



## Memory Map REQUIREMENTS

### Mapping



| Memory Section | Contents | Notes |

| --- | --- | --- |

| CurrMeasCorrln_START_SEC_CODE |  |  |



* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage



| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |



Table 1: ARM Cortex R4 Memory Usage

### Non  RTE NvM Blocks

Note : Size of the NVM block if configured in developer

### RTE NvM Blocks

Note : Size of the NVM block if configured in developer

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None
